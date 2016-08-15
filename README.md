docker-drupal-brightcove
==============

This is a recipe for building a [Docker](https://www.docker.com/) container with Drupal 7 and the latest Brightcove module (7.x-6.x), including Linux (Debian 8), Apache and MySQL.
Before building, make sure you have [Docker Engine](https://docs.docker.com/engine/installation/) installed.

Based on: https://github.com/ricardoamaro/docker-drupal

Note: in order for uploading to work, the Drupal site must be accessible from the internet - because uploaded videos/images/captions are first stored on your Drupal site before being retrieved by Brightcove.

### How to use:

```sh
git clone https://github.com/janmashat/docker-drupal-brightcove.git
cd docker-drupal-brightcove

docker build -t drupal-bc .
docker run -it --name drupal-bc -p 80:80 -p 9001:9001 drupal-bc
```

If you would like to store the docroot on the host:

```sh
docker run -it --name drupal-bc -p 80:80 -p 9001:9001 -v path_on_the_host:/var/www drupal-bc
```
