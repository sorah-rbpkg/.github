# sorah-rbpkg

[@sorah](https://github.com/sorah)'s Ruby binary packages for Ubuntu and Debian.

Package sources are based on [Debian Ruby Team's work](https://salsa.debian.org/ruby-team) and maintained to keep closer to them. However, because of version disparity, most `ruby-*` Debian package are not expected to work with. You'll find sorah-rbpkg sourced packages useful to spin your own application.

Note: This repository is not supported by Ruby core team. Maintained by Sorah, a Ruby committer, individually.

## Packages

- [rubyN.M](https://github.com/sorah-rbpkg/ruby) (e.g. ruby2.7, ruby3.0, ruby3.1, ruby3.2, ...)
- [ruby-defaults](https://github.com/sorah-rbpkg/ruby-defaults) (ruby, libruby, ruby-dev)
- [rubygems-integration](https://github.com/sorah-rbpkg/rubygems-integration)

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
- Pinning src:ruby-defaults is recommended to avoid unintended upgrading Ruby series.

## Build by your own

These packages are built with the following scripts, you may use these to reproduce:

- https://github.com/sorah/config/blob/master/bin/sorah-debuild
- https://github.com/sorah/config/blob/master/bin/sorah-debuild-codebuild
- https://github.com/sorah/config/blob/master/bin/sorah-debuild-auto

## Caveats

- YJIT is enabled.

## See also

https://sorah.jp/packaging/debian/
