# corpus
A suite of text corpus preprocessing tools for validating, cleaning, and converting raw text corpora into tabular data.

## Documentation
```
corpus - A suite of tools for cleaning textual corpora. 
Usage: corpus SUBCOMMAND [ARGUMENTS...]

Subcommands:
	--help|-h|help [SUBCOMMAND]	Prints help text for SUBCOMMAND. If SUBCOMMAND omitted, prints list of subcommands.
	charset [FILE...]	Prints counts of every character used in the corpus, substituting ASCII octal codes for control characters. Also counts filename metadata if corpus merged.
	detokenize [FILE...]	Compresses a list of tokens back into lines of text. Currently ignores linebreaks and creates one continuous stream of tokens.
	kwic KEYWORD [FILE...]	Keywords in context. Print all windows of which KEYWORD falls in the center.
	mangle UNIGRAM [BIGRAM [WINDOW=1]]	Mangles all UNIGRAM if BIGRAM not supplied, otherwise all bigrams formed from UNIGRAM and BIGRAM within WINDOW of each other in a line-separated TOKENS file.
	merge FILE...	Merges FILES together with file separator bytes so that they can be streamed.
	mwe MWE...	Replace all multiword expressions MWE in the corpus on stdin with single tokens joined by a separator.
	split 	Splits apart a merged file stream and writes it to separate files.
	stopwords STOPWORDLIST FILE...	Removes stop words in STOPWORDLIST from tokenized FILE...
	tokens [FILE...]	Prints list of whitespace-separated tokens in the corpus.
	types [FILE...]	Prints list of unique token types in the corpus.
```
## TODO
- Make mwe match multiline expressions.
- Give merge option to split lines to make large token files readable by other line-based tools. Possibly using null bytes to preserve original linebreaks.
