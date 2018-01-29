# Check and build the docs for SmartSDK guided-tour

The SmartSDK guided tour is hosted at:

https://github.com/smartsdk/guided-tour

## Usage

### Build the image

``` shell
GUIDED_TOUR_BUILDER="guided-tour-builder"
docker build -t "${GUIDED_TOUR_BUILDER}" .
```

### Run the image

``` shell
docker run -it --rm -v $(pwd):/docs $GUIDED_TOUR_IMAGE
```

Expected output:

- if problems: error or warning from the md linter
- else: documentation build in `_build` directory
