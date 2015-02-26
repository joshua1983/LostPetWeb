# LostPetWeb
Pagina web LostPet

#configuracion apache:
	Alias /lost "D:/CODIGO_FUENTE/lostpet/LostPetWeb/webpet/public"
	    <Directory "D:/CODIGO_FUENTE/lostpet/LostPetWeb/webpet/public">
	        Options Indexes FollowSymLinks Includes ExecCGI
			AllowOverride All
			Order allow,deny
			Allow from all
			Require all granted
		</Directory>
	
#htaccess
	<IfModule mod_rewrite.c>
	    Options +FollowSymLinks
	    RewriteEngine On
	    RewriteBase /softrack
	</IfModule>
	
	<IfModule mod_rewrite.c>
	    RewriteCond %{REQUEST_FILENAME} !-f
	    RewriteCond %{REQUEST_FILENAME} !-d
	    RewriteRule ^(.*)$ index.php?/$1 [L]
	</IfModule>