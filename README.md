# RStudio

A minimal [RStudio](https://www.rstudio.com/) server container that
can be accessed that integrates well with
[Nuvla](https://docs.nuvla.io/).

## Supported tags and respective `Dockerfile` links

Multi-architecture tags: 

 - `latest` ([Dockerfile](https://github.com/nuvla/example-rstudio/blob/master/Dockerfile))

Architecture-specific tags:

 - `latest-amd64` ([Dockerfile](https://github.com/nuvla/example-rstudio/blob/master/Dockerfile))

## How to use this image

To run the container:

```sh
docker run -d -p 8080:80 nuvla/example-rstudio
```

You can then access the interface via your browser at a link like:

```
http://host:8080/
```

The username is 'rstudio' and the generated password is printed to the
console (and provided as a Nuvla output parameter).

Use the standard Docker commands to stop and remove the container.

## How to build this image

To build the container on your current platform, clone the sources
from the
[nuvla/example-rstudio](https://github.com/nuvla/example-rstudio)
GitHub, then run the following Docker command:

```sh
docker build . --tag nuvla/example-rstudio
```

To build the container for all supported platforms, run the commands:

```sh
./.travis.before_install.sh
./.travis.script.sh
```

The `before_install.sh` script may not be necessary if "binfmt_misc"
support is already included in your Docker installation (e.g. MacOS).
