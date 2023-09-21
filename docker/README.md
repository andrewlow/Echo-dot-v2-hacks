# Docker

When rooting the Echo Dot v2, it's helpful to do this in a container. The included Dockerfile creates a container with the [EchoCLI](https://github.com/Dragon863/EchoCLI) tools, adb, fastboot, and mtkclient. Everything that's needed to root the device and boot it.

## Usage

Build with:

`docker compose build echo`

Run with:

`docker compose run echo`

You can connect additional shells to this container with:

`docker exec -it echo /bin/bash`

Be aware that exiting the first shell will stop the container for all other shells.

The container contains 3 folders of interest, in addition to the `adb` and `fastboot` binaries:

* /EchoCLI - the EchoCLI tools
* /mtktools - the `mtk` script
* /work - any files and folders you would like mapped in to the container

