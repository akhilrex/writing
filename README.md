Writing
=======

**Writing** is a lightweight distraction-free text editor, in the browser.

This is a Fork of the Writing repo to add docker-compatibility.

<img src="http://i.imgur.com/c56hDwi.gif" />

Find the docker images here - hub.docker.com/r/akhilrex/writing

## Installation

The easiest way to run Writing is to run it as a docker container. 

### Using Docker

Simple setup without mounted volumes (for testing and evaluation)
```sh
  docker run -d -p 8080:80 --name=writing akhilrex/writing
```

### Using Docker-Compose

```yaml
version: "2.1"
services:
  writing:
    image: akhilrex/writing
    container_name: writing
    ports:
      - 8080:80
    restart: unless-stopped
```

Then simply run the following command

```sh
   docker-compose up -d
```