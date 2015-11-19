# Known

Known application for the Commons Cloud network

# How to use this image

The easiest is to use our `docker-compose.yml`.

Make sure you have [docker-compose](http://docs.docker.com/compose/install/) installed. And then:

```
git clone https://github.com/allmende/known.git allmende/known
cd allmende/known
# edit variables:
vim .env
vim docker-compose.yml
docker-compose up
```

After setting up [nginx-proxy](https://github.com/jwilder/nginx-proxy) you can access the instance on your machine.
=======
You can now access your instance on the port 80 of the IP of your machine.

## Access it from Internet

We recommend the usage of SSL, so the easiest is to modify the `nginx.conf` file.

Once it is done, you can connect to the port of the host by adding this line to `docker-compose.yml`:
```
web:
...
  - ports:
    - "443:443"
    - "80:80"
...
```

## Installation

Once started, you'll arrive at the configuration wizzard.

## Backup

In order to backup, just run the `./BACKUP` script. And copy all the data to a safe place.
