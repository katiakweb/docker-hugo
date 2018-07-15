# Hugo

[![](https://images.microbadger.com/badges/image/klakegg/hugo.svg)](https://microbadger.com/images/klakegg/hugo "Get your own image badge on microbadger.com")
[![Build Status](https://travis-ci.org/klakegg/docker-hugo.svg?branch=master)](https://travis-ci.org/klakegg/docker-hugo)

Truly minimal Docker images for [Hugo](http://gohugo.io/) with batteries included.
These images sets `destination` during build and `bind` when started as server, otherwise no magic.


## Available tags

Default minimal image based upon [Busybox](https://hub.docker.com/r/_/busybox/):
* Hugo 0.44: `0.44-busybox`, `busybox`, `0.44`, `latest`, `0.44-busybox-onbuild`, `0.44-onbuild`, `busybox-onbuild`, `onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.44/busybox/Dockerfile-busybox))
* Hugo 0.43: `0.43-busybox`, `0.43`, `0.43-busybox-onbuild`, `0.43-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.43/busybox/Dockerfile-busybox))
* Hugo 0.42.2: `0.42.2-busybox`, `0.42.2`, `0.42.2-busybox-onbuild`, `0.42.2-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42.2/busybox/Dockerfile-busybox))
* Hugo 0.42.1: `0.42.1-busybox`, `0.42.1`, `0.42.1-busybox-onbuild`, `0.42.1-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42.1/busybox/Dockerfile-busybox))
* Hugo 0.42: `0.42-busybox`, `0.42`, `0.42-busybox-onbuild`, `0.42-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42/busybox/Dockerfile-busybox))

Minimal image based upon [Alpine](https://hub.docker.com/r/_/alpine/):
* Hugo 0.44: `0.44-alpine`, `alpine`, `0.44-alpine-onbuild`, `alpine-onbuild`, `0.44-ext-alpine`, `ext-alpine`, `0.44-ext-alpine-onbuild`, `ext-alpine-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.44/alpine/Dockerfile-alpine))
* Hugo 0.43: `0.43-alpine`, `0.43-alpine-onbuild`, `0.43-ext-alpine`, `0.43-ext-alpine-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.43/alpine/Dockerfile-alpine))
* Hugo 0.42.2: `0.42.2-alpine`, `0.42.2-alpine-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42.2/alpine/Dockerfile-alpine))
* Hugo 0.42.1: `0.42.1-alpine`, `0.42.1-alpine-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42.1/alpine/Dockerfile-alpine))
* Hugo 0.42: `0.42-alpine`, `0.42-alpine-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42/alpine/Dockerfile-alpine))

Minimal image based upon [Alpine](https://hub.docker.com/r/_/alpine/) with [Asciidoctor](http://asciidoctor.org/) installed:
* Hugo 0.44: `0.44-asciidoctor`, `asciidoctor`, `0.44-asciidoctor-onbuild`, `asciidoctor-onbuild`, `0.44-ext-asciidoctor`, `ext-asciidoctor`, `0.44-ext-asciidoctor-onbuild`, `ext-asciidoctor-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.44/alpine/Dockerfile-asciidoctor))
* Hugo 0.43: `0.43-asciidoctor`, `0.43-asciidoctor-onbuild`, `0.43-ext-asciidoctor`, `0.43-ext-asciidoctor-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.43/alpine/Dockerfile-asciidoctor))
* Hugo 0.42.2: `0.42.2-asciidoctor`, `0.42.2-asciidoctor-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42.2/alpine/Dockerfile-asciidoctor))
* Hugo 0.42.1: `0.42.1-asciidoctor`, `0.42.1-asciidoctor-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42.1/alpine/Dockerfile-asciidoctor))
* Hugo 0.42: `0.42-asciidoctor`, `0.42-asciidoctor-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.42/alpine/Dockerfile-asciidoctor))

Image based upon [Debian](https://hub.docker.com/r/_/debian/):
* Hugo 0.44: `0.44-debian`, `debian`, `0.44-debian-onbuild`, `debian-onbuild`, `0.44-ext`, `ext`, `latest-ext`, `0.44-ext-debian`, `ext-debian`, `0.44-ext-debian-onbuild`, `ext-debian-onbuild`, `0.44-ext-onbuild`, `ext-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.44/debian/Dockerfile-debian))
* Hugo 0.43: `0.43-debian`, `0.43-debian-onbuild`, `0.43-ext-debian`, `0.43-ext-debian-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.43/debian/Dockerfile-debian))

Image based upon [Ubuntu](https://hub.docker.com/r/_/ubuntu/):
* Hugo 0.44: `0.44-ubuntu`, `ubuntu`, `0.44-ubuntu-onbuild`, `ubuntu-onbuild`, `0.44-ext-ubuntu`, `ext-ubuntu`, `0.44-ext-ubuntu-onbuild`, `ext-ubuntu-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.44/ubuntu/Dockerfile-ubuntu))
* Hugo 0.43: `0.43-ubuntu`, `0.43-ubuntu-onbuild`, `0.43-ext-ubuntu`, `0.43-ext-ubuntu-onbuild` ([Dockerfile](https://github.com/klakegg/docker-hugo/blob/0.43/ubuntu/Dockerfile-ubuntu))

Looking for older tags? Please see the [complete list of tags](https://github.com/klakegg/docker-hugo/blob/master/tags.md).


## Using image

This image does not try to do any fancy.
Users may use Hugo just as they are used to.

The good practice of having a separate output folder is part of the image.


### Ordinary use

Normal build:

```
docker run --rm -it -v $(pwd):/src -v $(pwd)/output:/target klakegg/hugo:0.44
```

Run server:

```
docker run --rm -it -v $(pwd):/src -p 1313:1313 klakegg/hugo:0.44 server
```


### docker-compose

Normal build:

```yaml
  build:
    image: klakegg/hugo:0.44
    volumes:
      - .:/src
      - ./output:/target
```

Run server:

```yaml
  server:
    image: klakegg/hugo:0.44
    command: server
    volumes:
      - .:/src
    ports:
      - 1313:1313
```


## Hugo shell (new as of 0.41)

A Hugo shell is made available in the Alpine/Debian/Ubuntu images (including Asciidoctor image).
Hugo shell is bash and Hugo completion.

When Alpine images are used is bash installed as part of initiation to minimize size of Docker image.

To get into a shell for your site:

```
docker run --rm -it -v $(pwd):/src klakegg/hugo:0.44-alpine shell
```


## Hugo extended edition (new as of 0.43)

Hugo as of version [0.43](https://github.com/gohugoio/hugo/releases/tag/v0.43) contains also an extended edition.

The extended edition is used in those images containing "ext" in the name. Except use of extended edition are those images exactly the same as those using the normal edition.

Table of Hugo extention features and the version when images first support the feature:

| Feature       | Alpine | Busybox | Debian | Ubuntu |
| ------------- | ------ | ------- | ------ | ------ |
| Hugo extended | 0.43   | -       | 0.43   | 0.43   |
| PostCSS       | -      | -       | 0.43   | 0.43   |


## Using an ONBUILD image

The onbuild images adds content of the folder of your Dockerfile into `/src` and builds to the `/onbuild` folder.

Example Dockerfile for your project where the site is made into an nginx image (Docker 17.05-ce or newer):

```Dockerfile
FROM klakegg/hugo:0.44-onbuild AS hugo

FROM nginx
COPY --from=hugo /onbuild /usr/share/nginx/html
```


## Using Pandoc

Hugo images with Pandoc support are made available for users wanting to use Pandoc in combination with Hugo.

[Hugo triggers Pandoc](https://gohugo.io/content-management/formats/#additional-formats-through-external-helpers) with `pandoc --mathjax`.
Some users may want to use other arguments, so to accommodate such a need is an alias `pandoc` created with the content of `HUGO_PANDOC` (default: `pandoc-default`) upon initiation.
The normal `pandoc` executable is renamed to `pandoc-default` to allow for later introduction of `pandoc-citeproc` if needed.

Example of explicit setting `pandoc` alias:

```
docker run --rm -it -v $(pwd):/src -v $(pwd)/output:/src/public -e HUGO_PANDOC="pandoc-default --strip-empty-paragraphs" klakegg/hugo:0.44-pandoc
```


## Overriding entrypoint

Those wanting to override entrypoint in the image may easily do so.

On command line using `--entrypoint`:

```
docker run --rm -it -v $(pwd):/src -v $(pwd)/output:/src/public --entrypoint hugo klakegg/hugo:0.44
```

In docker-compose using `entrypoint`:

```yaml
  build:
    image: klakegg/hugo:0.44
    entrypoint: hugo
    volumes:
      - .:/src
      - ./output:/src/public
```


## Configuration

Environment variables:
* HUGO_BIND - Bind address for server. Default: `0.0.0.0`
* HUGO_DESTINATION - Location of output folder. Default: `/target`
* HUGO_PANDOC - Pandoc command to be triggered. Default: `pandoc-default`

Volumes:
* ```/src``` - Source folder and workdir
* ```/target``` - Target folder

Ports:
* 1313/tcp
