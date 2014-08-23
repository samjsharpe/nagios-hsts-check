#  check_hsts_headers

A nagios check which checks for validity of the HTTP Strict-Transport-Security header.

## Requirements

Nagios or Icinga, Python (with the argparse, sys and urllib2 modules)

## Usage

```
$ ./check_hsts_headers --help
usage: check_hsts_headers [-h] --url URL [--maxage MAXAGE]
                          [--username USERNAME] [--password PASSWORD]
                          [--realm REALM]

Check for Strict-Transport-Security header

optional arguments:
  -h, --help           show this help message and exit
  --url URL            the URL to check
  --maxage MAXAGE      optional expected max-age value
  --username USERNAME  optional username
  --password PASSWORD  optional password
  --realm REALM        optional realm for basic auth
```
