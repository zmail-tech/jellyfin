# jellyfin
Docker compose deployment using nginx proxy with letsencrypt companion

# Requirements
This requires a running version of jwilder's NGINX with LE proxy companion such
as the version on my github zmail-tech/nginx-le

# How to Deploy
To deploy this docker image simply edit the .env file with the appropriate values.
You will need to point a DNS record to the server you wish to deploy this from
and enter the domain you specified into the VIRTUAL_HOST variable.

The email variable is the account you want to receive LE alerts to.

Next make your media files available in the project directory. I recommend using
symbolic links

Example (Run from project directory):
> ln -s /path/to/your/movies ./movies
> ln -s /path/to/your/tvshows ./tvshows

Next run docker compose up
> docker-compose up -d
