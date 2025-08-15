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
| Linux kernel headers | 6.12.41 |
| GNU Binutils         | 2.45    |

The `extended`-tagged image contains, in addition to the tools above:

| Tool / Library | Version |
| -------------- | ------- |
| zlib           | 1.3.1   |
| OpenSSL        | 3.5.2   |
| curl           | 8.15.0  |
| Git            | 2.50.1  |
| CMake          | 4.1.0   |
| Python         | 3.13.6  |

## License

This project is [MIT-licensed](LICENSE).
