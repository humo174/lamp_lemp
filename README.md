# LAMP/LEMP via Docker

<h2>LEMP</h2>
<h3>Services</h3>
<ul>
  <li>Nginx</li>
  <li>PHP-FPM</li>
  <li>MariaDB</li>
  <li>PhpMyAdmin</li>
  <li>Adminer (Need uncomment in compose file)</li>
</ul>
<h3>Development</h3>
<code>docker compose -f docker-compose-lemp.yaml up -d</code>
<h2>LAMP</h2>
<h3>Services</h3>
<ul>
  <li>Apache Httpd Server</li>
  <li>PHP-FPM</li>
  <li>MariaDB</li>
  <li>PhpMyAdmin</li>
  <li>Adminer (Need uncomment in compose file)</li>
</ul>
<h3>Development</h3>
<code>docker compose -f docker-compose-lamp.yaml up -d</code>
