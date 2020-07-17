
# awdns - Command line DNS admin tool for AWS

Create, update and delete DNS records and zones hosted at AWS.

## Motivation

AWS console and official CLI are both powerful, yet complicated.   awdns
is a simple CLI tool to ease the burden of administering Route53 DNS
domains for the most popular DNS records (A, AAAA).

## Features

* List all zones
* List all records in a zone
* Add a record to a zone

## Examples

Add a new record.
```
$ ./bin/awdns add foo4.example.com 127.0.0.1
```

Delete one or more records.
```
$ ./bin/awdns del foo4.example.com
```

## Installation

```
$ git clone https://github.com/bloq/awdns.git
$ cd awdns
$ npm i
$ ./bin/awdns ...

