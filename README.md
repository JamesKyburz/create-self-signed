# create-self-signed

A Docker image that will create self signed certificates.

<a href="https://asciinema.org/a/4s9cilquvukowdlzfqpetp371?autoplay=1"><img src="https://asciinema.org/a/4s9cilquvukowdlzfqpetp371.png" width="380"/></a>

# usage

```sh
docker run --rm \
  -e ALTNAME='DNS:local.awesome.com' \
  -e CN='*.awesome.com' \
  -v=$(pwd)/certs-output:/certs jameskyburz/create-self-signed:latest
```

## custom filenames

```sh
docker run --rm \
  -e PRIVKEY_FILENAME='my_privkey.key' \
  -e CERT_FILENAME='my_cert.pem' \
  ...
```

# why?

All of my self signed certificates stopped working since the last OSX security update :(

Also I wanted a single solution to be able to create certificates on OSX, Linux & Windows, docker to the rescue!

Docker images hosted at https://hub.docker.com/r/jameskyburz/create-self-signed.

If you want multiple values in ALTNAME seperate with a ,

# license

[Apache License, Version 2.0](LICENSE)
