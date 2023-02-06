# sorah-rbpkg

<a href='https://ko-fi.com/J3J8CKMUU' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi3.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

[@sorah](https://github.com/sorah)'s Ruby binary packages for Ubuntu and Debian.


Package sources are based on [Debian Ruby Team's work](https://salsa.debian.org/ruby-team) and maintained to keep closer to them. This project aims to deliver major and stable releases early using APT without upgrading distributions or waiting new release of distributions. Because of version and branch disparity, most `ruby-*` Debian package are not expected to work with. You'll find sorah-rbpkg sourced packages useful to spin your own application.

Note: This repository is not supported by Ruby core team. Maintained by Sorah, a Ruby committer, individually.

## Packages

- [rubyN.M](https://github.com/sorah-rbpkg/ruby) (e.g. ruby2.7, ruby3.0, ruby3.1, ruby3.2, ...)
- [ruby-defaults](https://github.com/sorah-rbpkg/ruby-defaults) (ruby, libruby, ruby-dev)
- [rubygems-integration](https://github.com/sorah-rbpkg/rubygems-integration)

Matrix of supported series and distros: see https://github.com/sorah/config/blob/master/etc/debian-packages.txt.

## Docker image

https://gallery.ecr.aws/sorah/ruby

For details, go [dockerfiles](https://github.com/sorah-rbpkg/dockerfiles)

## Repository

```
deb https://cache.ruby-lang.org/lab/sorah/deb/ bionic main
deb https://cache.ruby-lang.org/lab/sorah/deb/ focal main
deb https://cache.ruby-lang.org/lab/sorah/deb/ stretch main
deb https://cache.ruby-lang.org/lab/sorah/deb/ buster main
deb https://cache.ruby-lang.org/lab/sorah/deb/ bookworm main
```

- Signed by [sorah-rbpkg (3F0F56A8)](https://sorah.jp/packaging/debian/3F0F56A8.pub.txt).
- You may also use the releases page of GitHub repos linked above to obtain a built package.
- Pinning src:ruby-defaults is recommended to select Ruby series (2.7, 3.0, 3.1, 3.2, ...) and prevent from unintended upgrade.

## Build by your own

These packages are built with the following scripts, you may use these to reproduce:

- https://github.com/sorah/config/blob/master/bin/sorah-debuild
- https://github.com/sorah/config/blob/master/bin/sorah-debuild-codebuild
- https://github.com/sorah/config/blob/master/bin/sorah-debuild-auto

## Caveats

- YJIT is enabled since Ruby 3.2.
- arm64 (aarch64) is available since Ruby 2.7.

## See also

https://sorah.jp/packaging/debian/
