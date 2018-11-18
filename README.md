# WPTricks
WordPress hacks, tips n tricks.

## [ .htaccess ] Hacks
```
php_value max_execution_time 60
php_value max_input_vars 3000
php_value upload_max_filesize 64M
php_value memory_limit 256M
```

Redirect old domain to new domain with URL match – .htaccess
```
RewriteEngine on
RewriteRule ^(.*)$ http://newdomain.com/$1 [R=301,L]
```
Redirect a single page
```
Redirect 301 /oldpage.html http://www.yoursite.com/newpage.html
Redirect 301 /oldpage2.html http://www.yoursite.com/folder/
```
Redirect an entire site.
* ✔ Intact links
* ✔ www.oldsite.com/some/crazy/link.html >> www.newsite.com/some/crazy/link.html
* ✔ Helpful for moving site to a new domain
* ❕ Place this on the OLD site's .htaccess

```
Redirect 301 / http://newsite.com/
```
