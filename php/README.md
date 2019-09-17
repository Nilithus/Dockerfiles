# PHP 7.3 docker image

This image installs php 7.3 on debian buildpack. Not meant for production deployments just for local development

## Usage
Mount your app at `/var/www/project` and bind a port on host to 80 on the container


```bash
#in app dir run
docker run -p 8888:80 -v `pwd`:/var/www/project {image-name}
```

## Customizing
If you want to customize php / run your own change the docker file. Just remember to update the php-fpm command in `config/supervisor.conf` to point to the new binary