#  check\_hsts\_headers

A Nagios check for the presence and lifetime of the HTTP
[Strict-Transport-Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) header.

## Requirements

Nagios or Icinga, Python3 with the `argparse`, `sys` and `requests` modules

## Usage

```
$ ./check_hsts_headers --help
usage: check_hsts_headers [-h] --url URL [--maxage MAXAGE]

Check for Strict-Transport-Security header

optional arguments:
  -h, --help       show this help message and exit
  --url URL        the URL to check
  --maxage MAXAGE  optional expected minimal value for max-age (default:
                   10368000 (i.e. 120 days))
```

## Notes

This check only looks at the HSTS header. Anything else is considered irrelevant
and is not taken into account. So whether the actual service works fine (200),
requires authentication (403), or even is failing (503 etc) is **not** checked.
