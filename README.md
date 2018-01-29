# Check and build the docs for SmartSDK guided-tour

The SmartSDK guided tour is hosted at:

https://github.com/smartsdk/guided-tour

## Usage

### Build the image by yourself (optional)

``` shell
GUIDED_TOUR_BUILDER="dancn/guided-tour-builder"
docker build -t "${GUIDED_TOUR_BUILDER}" .
```

### Run the image (using the image from https://hub.docker.com)

``` shell
GUIDED_TOUR_BUILDER="dancn/guided-tour-builder"
docker run -it --rm -v $(pwd):/docs $GUIDED_TOUR_IMAGE
```

Expected output:

- if problems: error or warning from the md linter
- else: documentation build in `_build` directory
