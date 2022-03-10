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
### 2) Pipeline
```bash
cd /gazelle/corpora && RAYON_NUM_THREADS=30 ungoliant pipeline /gazelle/corpora/ungoliant/1_download/ /gazelle/corpora/ungoliant/2_pipeline --lid-path /root/projects/ungoliant-dioco/lid.176.bin
```
### 3) Dedup