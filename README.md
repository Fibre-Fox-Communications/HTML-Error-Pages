# Fibre Fox Communications Error Pages

Static HTML error pages with a shared stylesheet.

Included: 400, 401, 403, 404, 408, 429, 500, 502, 503, 504.

Copy the HTML files and `styles.css` to your web root or configured error-page directory.

## Nginx example

```nginx
error_page 404 /404.html;
error_page 500 502 503 504 /500.html;
location = /404.html { internal; }
location = /500.html { internal; }
```

## Apache example

```apache
ErrorDocument 404 /404.html
ErrorDocument 500 /500.html
ErrorDocument 503 /503.html
```

## IIS example

Use IIS Manager > Error Pages > Edit Feature Settings, then map each status code to the matching HTML file.
