# pdfjs
It's a modified build of Mozilla pdf.js library. 
## How it works?
It allows to change the adress to view PDF file (e.g. `/document.pdf`) from 
`http://domain.com/web/viewer.html?file=/document.pdf`
to
`http://domain.com/document.pdf`

I changed all paths from relative to absolute, modified PDF file path (and added timestamp, so there is no problem with cache) and wrote a rewrite rule for nginx.

## How to use it?
Clone the repo in the root folder of your web server (so you have `web/` and `build/` folders in the `pdfjs/` folder), add the rewrite rule to your nginx config, restart the web server, everything should work. 
