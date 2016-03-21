# alpine-pkg-makeself

[![CircleCI](https://img.shields.io/circleci/project/sgerrand/alpine-pkg-makeself/master.svg)](https://circleci.com/gh/sgerrand/alpine-pkg-makeself)

This is the [Makeself][makeself] utility script as an Alpine Linux package.

## Releases

See the [releases page][releases] for the latest download links.

## Installing

The current installation method for these packages is to pull them in using
`wget` or `curl` and install the local file with the `--allow-untrusted` option
to `apk`:

```
apk --no-cache add ca-certificates
wget https://github.com/sgerrand/alpine-pkg-makeself/releases/download/2.2.0-r0/makeself-2.2.0-r0.apk
apk --allow-untrusted add makeself-2.2.0-r0.apk
```

[makeself]: http://www.megastep.org/makeself/
[releases]: https://github.com/sgerrand/alpine-pkg-makeself/releases/
