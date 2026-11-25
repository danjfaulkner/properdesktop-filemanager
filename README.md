# File Manager

Proper Desktop File Manager, simple to use, beautiful, and retain the classic PC interactive design.

<img src="screenshots/filemanager.png" alt="File Manager" width="945">

## Dependencies

File Manager is built on [properdesktop-toolkit](https://github.com/danjfaulkner/properdesktop-toolkit) and
the files library of [properdesktop-framework](https://github.com/danjfaulkner/properdesktop-framework);
install them first. The mount service needs FUSE, libssh, libsmbclient, libmtp and
libudev, and zlib, bzip2, liblzma and LZFSE for disk images; archives need libarchive
and libzip. GoogleTest for the tests.

Debian/Ubuntu:

```shell
sudo apt install build-essential cmake pkg-config libicu-dev libarchive-dev libzip-dev \
    libfuse3-dev libssh-dev libsmbclient-dev libmtp-dev libudev-dev zlib1g-dev libbz2-dev \
    liblzma-dev liblzfse-dev libgtest-dev
```

## Build

```shell
cmake -S . -B build -DCMAKE_INSTALL_PREFIX=/usr
cmake --build build
sudo cmake --install build
```

## Tests

```shell
cmake -S . -B build -DBUILD_TESTING=ON
cmake --build build
ctest --test-dir build --output-on-failure
```

## License

BSD-3-Clause; see [LICENSE](LICENSE).
