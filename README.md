# secure-messaging-compose

This repository allows you to spin up a local test environment for the ``secure-messaging-`` suite of services.

### Prerequisites

 - make
 - docker
 - docker-compose
 - git

### Getting started

Export a ``SECURE_MESSAGING_HOME`` environment variable. This should point at a folder into
which you wish to clone the rest of the services (e.g. ``/home/my-user/secure-messaging``)
[see [configuration](#configuration)]

Clone this repository somewhere and run ``make``

```shell
$ git clone git@github.com:qateam123/secure-messaging-compose.git
$ cd secure-messaging-compose
$ make
```

This will attempt to clone the repositories into ``SECURE_MESSAGING_HOME`` and run their ``Dockerfile``'s

Once built, you can bring the services up with:

```shell
$ make start
```

Rebuild services:

```shell
$ make build
```

### Configuration

``secure-messaging-compose`` is not a service in itself, but requires an environment variable
to build and run other services.

| Environment variable | Default | Description
| -------------------- | ------- | -----------
| SECURE_MESSAGING_HOME| _none_  | The folder to clone service repositories to
| PYTHON3              | _none_  | Path to python3 executable (e.g. ``/usr/local/bin/python3``).
