# fastq-utils

A collection of simple Bash utilities for working with FASTQ files.

## Scripts

### count_reads.sh

Counts the number of reads in all `.fastq.gz` files within a directory and outputs the results as a CSV file.

**Usage:**

```bash
bash count_reads.sh <fastq_directory> <output_file>
```

**Example:**

```bash
bash count_reads.sh /data/raw_fastq read_counts.csv
```

**Output format:**

```
File Name,Reads
sample_01,1500000
sample_02,2300000
```

### merge_fastq.sh

Merges multiple `.fastq.gz` files into a single compressed file and verifies the merge by comparing line counts.

**Usage:**

```bash
bash merge_fastq.sh <output_file> <input_file_1> <input_file_2> [input_file_3 ...]
```

**Example:**

```bash
bash merge_fastq.sh merged.fastq.gz sample_L001.fastq.gz sample_L002.fastq.gz sample_L003.fastq.gz
```

## Requirements

- `zcat`
- `gzip`
- `awk`

These are pre-installed on most Linux/macOS systems.

## Installation

```bash
git clone https://github.com/<your-username>/fastq-utils.git
cd fastq-utils
chmod +x *.sh
```
