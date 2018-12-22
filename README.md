# WPTricks
WordPress hacks, tips n tricks.

* [WordPress useful links](https://github.com/metaspook/OpenWebDir/blob/master/README.md#wordpress) - OpenWebDir
* [16 htaccess Hacks to Speed Up, Optimize and Secure WordPress](https://makeawebsitehub.com/wordpress-htaccess-hacks)
* [Increasing the WordPress Memory Limit](https://docs.woocommerce.com/document/increasing-the-wordpress-memory-limit)
* [How Do I Find php.ini File?](https://www.templatemonster.com/blog/where-is-php-ini)
* [Disable mod_security in .htaccess](https://stackoverflow.com/questions/12928360/how-can-i-disable-mod-security-in-htaccess-file)

## [ Object Cache file]
In case any object Cache tweak related to memchache, memchached, redis etc. or fix HTTP Error 500 like issue edit this file **"public_html/wp-content/object-cache.php"**. Note! in defference replace "public_html" dir with root directory of your WordPress.

#### Legends
- [x] = Tick
- [ ] = Untick

## [ PHP ] Hacks
|                | Object Cache | Assigned to   | Current Status | Finished | 
|----------------|---------------|---------------|----------------|-----------|
| **PHP Extensions** |<ul><li>[x] memcached</li><li>[x] redis</li></ul> | > 5 hours  | @georgehrke | in progress | - [x] ok?
| **PHP Options**   |   | php_value max_execution_time 60
php_value max_input_vars 5000
php_value upload_max_filesize 256M
php_value memory_limit 256M | in progress | [x] item1<br/>[ ] item2
| Object Cache   | > 5 hours  | @georgehrke | in progress | <ul><li>- [x] item1</li><li>- [ ] item2</li></ul>
| Object Cache   | > 5 hours  | @georgehrke | in progress | <ul><li>[x] item1</li><li>[ ] item2</li></ul>

## [ .htaccess ] Hacks
```
php_value max_execution_time 60
php_value max_input_vars 5000
php_value upload_max_filesize 256M
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
