# Docker image: wangkexiong/deno4centos7
![Docker Build Badge](https://github.com/wangkexiong/docker-deno4centos7/workflows/Docker%20Build/badge.svg)
![License](https://img.shields.io/github/license/wangkexiong/docker-deno4centos7)
![1.5.4](https://img.shields.io/docker/v/wangkexiong/deno4centos7/1.5.4?style=social)
![1.6.1](https://img.shields.io/docker/v/wangkexiong/deno4centos7/1.6.1?style=social)
![1.6.3](https://img.shields.io/docker/v/wangkexiong/deno4centos7/1.6.3?style=social)

## WHY?
[Deno project on github][] gives binary releases, but it depends on GLIBC_2.18.

And in REL7/CentOS7, the glibc libraries (libc/libm/libpthread/etc...) are based on the glibc2.17 release.
We can run the build on CentOS7 to make the binary that can work on CentOS7.

I run the project to make the docker image with new build deno binary on CentOS7.

```bash
$ docker run --rm wangkexiong/deno4centos7:1.5.4 cat /usr/local/bin/deno > deno
$ chmod +x deno
$ ./deno -V
deno 1.5.4
```


[Deno project on github]: https://github.com/denoland/deno
