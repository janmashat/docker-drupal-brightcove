docker-drupal-brightcove
==============

Docker image for Drupal 7.x with Brightcove 7.x-6.x.

Based on: https://github.com/ricardoamaro/docker-drupal

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
