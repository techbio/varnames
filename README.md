# Variable/Identifier Name Analysis
## *Source code is for humans*

This is a project I have been thinking about for some time, exploring an interest in the human communication aspects of programming, non-reserved keyword/syntax features of source that are determined by creative/appropriate human language identifiers.

Potentially find commonly misused or improvable naming patterns, identify high or low quality code/commits, look for patterns related to code authorship, training, or sibling projects.

Publish to pique the interest of other coders.

1. acquire repo/directory/files
1. read source code files
2. extract variables, array keys, function names
3. analyze strings
   - split multi-word names (ie. camelCase => camel case)
   - show list of files/projects containing one or more string
   - view as tag clouds
   - count occurences in corpus and per file, TF-IDF to relate "similar" files/projects
1. create a report


PHP is easy ($xxx, function xxx(...), ->xxx, ['xxx']) (Bash/Perl similar)

Java is pretty easy, with declarations ([scope] TypeName xxx, function xxx)

Other languages, not sure yet...should make use of native tooling, compilers, analysis, there may be libraries which extract these and more details from many/all languages

Request contributors to add modules/functions/scripts/ReST APIs to find identifiers in other programming languages
 (static analysis expert Bro Dave?)

analyze and report as above for PHP

## Prototype/Proof-of-Concept
[varnames.sh](./varnames.sh) - proof of concept with basic PHP variable regex only

[varnames.txt](./varnames.txt) - raw output

[varnames_word_parts.txt](./varnames_word_parts.txt) - after programming-case conversion tool

[varnames_word_parts_counts.txt](./varnames_word_parts_counts.txt) - word parts with corpus frequency

PoC corpus is from a number of URL shortener repos from GitHub (~700, but only a fraction of them in PHP, approximately 5000 PHP files)


## Beyond
1. attempt to classify source code application by its identifiers
6. vote for good/bad names
7. rate repo on naming readability and descriptive precision
1. charge $2 to navigate further into pre-analyzed codebases or ~$2/100Kb to request analysis for a repo
4. extend beyond PHP with existing static analyais tools/abstract syntax tree
