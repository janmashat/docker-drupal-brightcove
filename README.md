docker-drupal7-brightcove6
==============

This is a recipe for building a [Docker](https://www.docker.com/) container with [Drupal](https://www.drupal.org/) 7 and [Brightcove module](https://www.drupal.org/project/brightcove) 7.x-6.x in a LAMP environment (Debian GNU/Linux, Apache, MySQL).

### Prerequisites

* Before building, make sure you have [Docker Engine](https://docs.docker.com/engine/installation/) installed and running.
* For uploading to work, make sure your Drupal site is accessible from the internet (public IP address or port-forward) - because Brightcove will need to fetch all uploaded video/image/caption files from your Drupal site.

### How to use

```sh
git clone https://github.com/janmashat/docker-drupal7-brightcove6.git
cd docker-drupal7-brightcove6

docker build -t drupal7-brightcove6 .
docker run -it --name drupal7-brightcove6 -p 80:80 -p 9001:9001 drupal7-brightcove6
```

The session will start within a GNU screen, so you can `ctrl-a c` to create a new screen.

If you would like to store the docroot on the host, use this `docker run` command instead:

```sh
docker run -it --name drupal7-brightcove6 -p 80:80 -p 9001:9001 -v path_on_the_host:/var/www drupal7-brightcove6
```

### Credits

Based on: https://github.com/ricardoamaro/docker-drupal
