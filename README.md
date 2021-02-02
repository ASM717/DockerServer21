ft_server (docker server) 100%
=========================
Dockerfile that sets up an nginx server. It must run a Wordpress with a MySQL database and and PHPMyAdmin.
How to use it

Make sure Docker Desktop is running and you are in the docker_server directory.

To build the docker image, run :

	docker build -t server .

The image is now created. To start an instance of it, run :

	docker run -p 80:80 -p 443:443 -d server
------------------------------------------------------------
If you want to switch autoindex(on \ off) -> cd etc/nginx/sites-availiable/default (open file with VIM) 
and correct this. Next you should use /nginx -s reload 
