# seffyroff/grav-caddy-docker

![grav](https://getgrav-grav.netdna-ssl.com/user/pages/media/grav-logo.svg)

[![Docker Automated buil](https://img.shields.io/docker/automated/seffyroff/grav-caddy-docker.svg)](https://hub.docker.com/r/seffyroff/grav-caddy-docker)

Grav is a Fast, Simple, and Flexible file-based Web-platform. There is Zero installation required. Although Grav follows principles similar to other flat-file CMS platforms, it has a different design philosophy than most.

The underlying architecture of Grav is built using well established and best-in-class technologies. This is to ensure that Grav is simple to use and easy to extend. Some of these key technologies include:

* Twig Templating: for powerful control of the user interface
* Markdown: for easy content creation
* YAML: for simple configuration
* Parsedown: for fast Markdown and Markdown Extra support
* Doctrine Cache: for performance
* Pimple Dependency Injection Container: for extensibility and maintainability
* Symfony Event Dispatcher: for plugin event handling
* Symfony Console: for CLI interface
* Gregwar Image Library: for dynamic image manipulation

## What is seffyroff/grav?

A Docker image with Grav CMS and PHP/Caddy.

Two versions of the container exist.  The default image is completely unmodified basic Grav out of the box.  For those looking to get something more functional there's a :admin tagged container which adds the admin interface in.  From there you've got a nice /admin interface to install and extend everything else if the cli isn't your best friend.

## Container Information

+ yobasystems/alpine-caddy:php image
+ fork from dsavell/grav Dockerfile
+ Port 2015 Exposed
+ No Custom Features by default
+ :admin container available with admin plugin installed

## Usage

```
docker create --name=grav \
--restart=always \
seffyroff/grav-caddy-docker
docker start grav
```

## Setting up the application
Access the webui at `http://<your-ip>:2015`, for more information check out [GRAV](https://getgrav.org/)

## Using the container

+ Shell Access to container when it is running: `docker exec -it grav /bin/sh`

## Issues

+ Pondering rebasing so no dependency on upstream image exists

## Changelog
+ **06/08/2017:** Added :admin tag
	- container configuration with admin interface installed available with :admin tag
+ **05/08/2017:** Initial Fork from dsavell/grav
	- Replaced Nginx with Caddy
	- Changed method of installing Grav to use composer instead of curling the zip
	- Typo corrections on the README.md
