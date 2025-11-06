add this to root htaccess:

<IfModule mod_rewrite.c>
  RewriteEngine On

  RewriteCond %{REQUEST_URI} ^/assets/Uploads/ [NC]
  RewriteCond %{REQUEST_URI} !^/index\.php
  RewriteRule ^ /index.php [L,QSA]
</IfModule>