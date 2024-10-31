# buildpack-deps

This repository contains Docker images that ship the latest common build tools
and libraries on legacy systems.
They are useful for building software that target a wide range of systems,
including legacy ones.

## Images

The images are available on Docker Hub as
[`zhongruoyu/buildpack-deps`](https://hub.docker.com/r/zhongruoyu/buildpack-deps).

Currently, only x86_64 images are provided.
They are based on the `debian/eol:wheezy` image, which provides glibc 2.13.
This version of glibc is compatible with most legacy systems that are still in
use today.

Two tags are provided: `base` and `extended`.

The `base`-tagged image contains the basic tools, including:

| Tool / Library       | Version |
| -------------------- | ------- |
| GCC                  | 14.2.0  |
| GNU Make             | 4.4.1   |
| Linux kernel headers | 6.6.58  |
| GNU Binutils         | 2.43.1  |

The `extended`-tagged image contains, in addition to the tools above:

| Tool / Library | Version |
| -------------- | ------- |
| zlib           | 1.3.1   |
| OpenSSL        | 3.4.0   |
| curl           | 8.10.1  |
| Git            | 2.47.0  |
| CMake          | 3.30.5  |
| Python         | 3.13.0  |

## License

This project is [MIT-licensed](LICENSE).
