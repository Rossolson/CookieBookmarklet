# CookieBookmarklet

This [bookmarklet](https://en.wikipedia.org/wiki/Bookmarklet) will create a web cookie from your Bookmarks Bar.

## Manual Installation

1) Create a bookmark on your Bookmark Bar/Favorites Bar of any page.
2) Rename the bookmark to ‘CookieFactory’ or something else you like.
3) Edit the address of the bookmark and paste the following code:

```
javascript:n=(prompt("Name","Example%20Cookie")+"=");v=escape(prompt("Value","Test%20Value"));p=(";%20path="+prompt("Path","/"));e=prompt("Expires?%20Blank%20for%20never",new%20Date().toUTCString());document.cookie=n+v+p+(e===""?"":";%20expires="+e);
```

## Quick Installation

[CookieFactory](javascript:n=(prompt("Name","Example%20Cookie")+"=");v=escape(prompt("Value","Test%20Value"));p=(";%20path="+prompt("Path","/"));e=prompt("Expires?%20Blank%20for%20never",new%20Date().toUTCString());document.cookie=n+v+p+(e===""?"":";%20expires="+e);)

## Activation

When you click on the Bookmark, it will ask you 4 sequential questions: Name, Value, Path and Expiration Date.

## Customization

It is straightforward to remove any of the 4 questions and have them default to a static or empty value. You must be careful. Bookmarklets are fragile: They’re URL-encoded JavaScript that run in an unknown context and must be less than 1024 characters.

This version will only ask you for the Name and Value, set the path to '/' and leave the Expiration Date to be the end of the current session:

`javascript:n=(prompt("Name","Example%20Cookie")+"=");v=escape(prompt("Value","Test%20Value"));p="";e="";document.cookie=n+v+p+(e===""?"":";%20expires="+e);`

This next version will only ask you for the Value, set the name to 'Custom Cookie', set the path to '/' and leave the Expiration Date to be the end of the current session:

`javascript:n="Custom%20Cookie"+"=");v=escape(prompt("Value","Test%20Value"));p="";e="";document.cookie=n+v+p+(e===""?"":";%20expires="+e);`

