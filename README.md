# create-self-signed

A Docker image that will create self signed certificates.

# usage

```sh
docker run --rm \
  -e ALTNAME='DNS:local.awesome.com' \
  -e CN='*.awesome.com' \
  -v=$(pwd)/certs-output:/certs jameskyburz/create-self-signed:latest
```

Docker images hosted at https://hub.docker.com/r/jameskyburz/create-self-signed.

If you want multiple values in ALTNAME seperate with a ,

# license

[Apache License, Version 2.0](LICENSE)
