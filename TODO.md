
* Support pagination of record lists
* Batch removal:  Multiple FQDNs on 'del' command line
* Batch add options:
	* pairs supplied via CLI args
	* pairs supplied via stdin
	* pairs supplied via CLI options
* Limit removal by RR type, to enable more fine-grained admin,
  and to avoid risking unintentional over-removal.

