
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
* Delete records from a zone
* Terse Unix responses (default) or verbose JSON responses.

## Examples

List all zones in the AWS account.

```sh
awdns zones
```

List all zones in the AWS account, with JSON output.

```sh
awdns --verbose zones
```

List all records associated with a single zone, in a BIND-like format.

```sh
awdns ls example.com
```

Add a new record, to a pre-existing zone in the AWS account.

```sh
awdns add foo4.example.com 127.0.0.1
```

Delete *all* records matching NAME, from a pre-existing zone in the AWS account.

```sh
awdns del foo4.example.com
```

## Usage

AWS authentication is handled via the AWS JavaScript SDK ([Credential details here.](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/setting-credentials-node.html)).

Full usage documentation via `--help` on the command line:

```console
$ awdns --help
Usage: awdns [options] [command]

Options:
  -V, --version         output the version number
  --ttl <num>           Specify TTL for new records (default: 300)
  --verbose             Enable verbose responses
  -h, --help            display help for command

Commands:
  add <FQDN> <address>  Add A or AAAA record to zone
  del <FQDN>            Delete all RRs from a zone with given FQDN
  ls <DOMAIN>           List all records for zone
  zones                 List all zones
  help [command]        display help for command
```

## Installation

```sh
npm install --global awdns
```
