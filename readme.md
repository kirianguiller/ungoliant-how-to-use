# Ungoliant Pipeline
https://github.com/oscar-corpus/ungoliant
This repo is a ùore personalized doc for using Ungoliant
## Installation
### Install Rust and Cargo
https://doc.rust-lang.org/cargo/getting-started/installation.html
### Install Ungoliant
Via git (via cargo is broken)
```bash
cargo install --git https://github.com/oscar-corpus/ungoliant
```

## Processing Pipeline
### Download paths 
```
wget https://commoncrawl.s3.amazonaws.com/crawl-data/CC-MAIN-2022-05/wet.paths.gz
zcat wet.paths.gz > wet.paths
```
### Download documents
```bash
ungoliant download ./wet.paths /gazelle/corpora/ungoliant/downloads/
```
### ???