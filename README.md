# Publication and acceptance times for journals with a focus on PLOS

This repository investigates the delays involved with scientific journal publications. The focus is on PLOS journals and other open access bioinformatics journals. This repository is home to the analyses for the blog post "[Publication delays at PLOS and 3,475 other journals](http://blog.dhimmel.com/plos-and-publishing-delays/)".

Pubmed is the main resource where articles and their dates are retrieved from. Pubmed records are easily accessible using the [Entrez E-utilities API](http://www.ncbi.nlm.nih.gov/books/NBK25500/). We also scraped the PLOS website as an orthogonal methodology for article date collection.

**Definitions**: Article *publication time* is the days from acceptance to epublication. Article *acceptance time* is the days for receival to acceptance.

## Publication and acceptance times for all journals since 2014

We retrieved pubmed records for all articles since 2014. The following datasets descend from this query:

+ [`data/pubmed-since-2104.tsv.gz`](data/pubmed-since-2104.tsv.gz) for a minimally processed table of pubmed records
+ [`data/pubmed-since-2014-filtered.tsv.gz`](data/pubmed-since-2014-filtered.tsv.gz) for a more processed table of pubmed records where publication and acceptance times were successfully computed.
+ [`data/pubmed-since-2014-summary.tsv`](data/pubmed-since-2014-summary.tsv) for a table where each row is a journal. For each journal, this table reports the mean, median, max, and min publication and acceptance times as well as number of articles contributing to the calculation. **_Check this resource to avoid throwing your manuscript into a black hole!_**

## Publication and acceptance times for PLOS journals

Two datasets of PLOS articles and their timestamps were created:

+ [`data/scraped-plos.tsv`](data/scraped-plos.tsv) for receival, acceptance, and publication dates scraped from the PLOS website. This file contains only a small subset of all PLOS articles, but may be more reliable because it is taken directly from the source.
+ [`data/pubmed-plos.tsv.gz`](data/pubmed-plos.tsv.gz) for scraped pubmed records for PLOS articles.
