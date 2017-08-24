# BASIC: BCR Assembly from SIngle Cells
Version: 1.0.1 (July, 15, 2016)

This repository has been forked from [Canzar et al. 2016](https://academic.oup.com/bioinformatics/article/33/3/425/2584479/BASIC-BCR-assembly-from-single-cells)

## Install

Pre-requisites and Installation
* BASIC was developed and tested using Python 3.4.4 and 2.7.10
* BASIC requires Bowtie2 to run.

## Usage

NOTE: The /db/ folder must remain alongside the BASIC.py file

Run `python BASIC.py -h` to display usage

```
usage: BASIC.py [-h] [-i TYPE] [-p CONSTANT_VALUE] [-n NAME] [-SE FASTQ]
                [-PE_1 LEFT] [-PE_2 RIGHT] [-g GENOME] [-b BOWTIE]
                [-o OUTPUT_LOCATION] [-v] [--version]

optional arguments:
  -h, --help          show this help message and exit
  -i TYPE             BCR, TCR, or HLA (default: BCR)
  -p CONSTANT_VALUE   Launch p > 2 threads that will run on separate
                      processors/cores (default: 2)
  -n NAME             Name of output file (default: result)
  -SE FASTQ           Single end FASTQ file. (example: se.fastq)
  -PE_1 LEFT          Paired end (left) FASTQ file. -PE_2 is required and
                      pairs must match order. (example: pe_1.fastq)
  -PE_2 RIGHT         Paired end (right) FASTQ files. (example: pe_2.fastq)
  -g GENOME           hg19 or mm10 (default: hg19)
  -b BOWTIE           Absolute path to directory that contains the bowtie2
                      executable
  -o OUTPUT_LOCATION  Output dir (default: none -- current working directory)
  -v                  Turns on verbosity (more details)
  --version           show program's version number and exit
```
Example: `python BASIC.py -b <path to Bowtie2> -SE A1_001.fastq.gz` 

### For further information check out the author's  [manual](http://ttic.uchicago.edu/~aakhan/BASIC/)

Please contact the original author for any questions or comments: aakhan@ttic.edu

License
Software provided to academic users under MIT License
