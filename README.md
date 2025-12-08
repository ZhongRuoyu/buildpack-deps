# buildpack-deps

This repository contains Docker images that ship the latest common build tools
and libraries on legacy systems.
They are useful for building software that target a wide range of systems,
including legacy ones.

## Images

The pre-built images are available on Docker Hub as
[`zhongruoyu/buildpack-deps`](https://hub.docker.com/r/zhongruoyu/buildpack-deps).

The x86_64 images are based on the `debian/eol:wheezy` image, which provides
glibc 2.13.
This version of glibc is compatible with most legacy systems that are still in
use today.

The AArch64 images are based on the `centos:7` image, which provides glibc 2.17.
This version of glibc is the first that supports AArch64.

Two tags are provided: `base` and `extended`.

The `base`-tagged image contains the basic tools, including:

| Tool / Library       | Version |
| -------------------- | ------- |
| GCC                  | 15.2.0  |
| GNU Make             | 4.4.1   |
| Linux kernel headers | 6.12.61 |
| GNU Binutils         | 2.45.1    |

The `extended`-tagged image contains, in addition to the tools above:

| Tool / Library | Version |
| -------------- | ------- |
| zlib           | 1.3.1   |
| OpenSSL        | 3.6.0   |
| curl           | 8.17.0  |
| Git            | 2.52.0  |
| CMake          | 4.2.1   |
| Python         | 3.13.9  |

## License

This project is [MIT-licensed](LICENSE).
