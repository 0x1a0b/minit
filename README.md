# minit

[![Build Status](https://travis-ci.org/yankeguo/minit.svg?branch=master)](https://travis-ci.org/yankeguo/minit)

**WORKING IN PROGRESS**

minimal init daemon for container, supports systemd service files

## Usage

```bash
minit redis nginx php-fpm
```

`minit` searchs `/etc/systemd/system`, `/lib/systemd/system`, `/usr/lib/systemd/system` for `redis.service`, `nginx.service` and `php-fpm.service` and run them.

`minit` IGNORES dependencies (`Requires=`, `After=`) BY DESIGN, because in most circumstances, they are not suitable for container environment.

## License

Yanke Guo <guoyk.cn@gmail.com>, MIT License
