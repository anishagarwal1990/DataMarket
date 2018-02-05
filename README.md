# DataMarket

From the top level directory of the repository, build the base docker file:
`docker build . -f docker/Dockerfile.dev.base -t datamart/devbase:0.1.0`

Then build your docker image for local development (change the tag if needed):
`docker build . -f docker/Dockerfile.dev -t datamart/dev`

Edit `docker/Dockerfile.dev` to change the tag name and rebuild the base image with a new version whenever you send a Pull Request (PR). Also build the release image and run tests:
```
docker build . -f docker/Dockerfile.release -t datamart/release
docker run datamart/release
```

TODO: So far there are no tests.
