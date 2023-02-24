# corpus
A suite of text corpus preprocessing tools

** Documentation
```
corpus - A suite of tools for cleaning textual corpora. 
Usage: corpus SUBCOMMAND [ARGUMENTS...]

Subcommands:
	--help|-h|help [SUBCOMMAND]	Prints help text for SUBCOMMAND. If SUBCOMMAND omitted, prints list of subcommands.
	merge FILE...	Merges FILES together with file separator bytes so that they can be streamed.
	mwe MWE...	Replace all multiword expressions MWE in the corpus on stdin with single tokens joined by a separator.
	split 	Splits apart a merged file stream and writes it to separate files.
```
## TODO
- Make mwe match multiline expressions.
