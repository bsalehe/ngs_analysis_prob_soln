## Errors and fixes during NGS analyses 

This repository describes issues and fixes when working with next genration sequencing data. It covers several issues primarily errors or bugs in running pipelines, tools including shell scripts related errors and their fixes.

### Error: FastQC ¨...java.lang.OutOfMemoryError: GC overhead limit exceeded¨
Normally this error occurs when allocated memory is too small to handle for instance long reads data

### Fix
In your FastQC command include -t 2 option as directed here: https://github.com/s-andrews/FastQC/issues/24

Example:

cat ../long_reads/*.fastq | fastqc -t 3 stdin:long_reads


