This repository describes issues and solutions when working with next genration sequencing data. It covers several issues primarily dealing with errors or bugs in running pipelines, tools including shell scripts related errors.

### FastQC ¨java.lang.OutOfMemoryError: GC overhead limit exceeded¨ error
Normally this error occurs when allocated memory is too small to handle for instance long reads data

### Soln
In your FastQC command include -t 2 options as directed here: https://github.com/s-andrews/FastQC/issues/24

Example:

cat ../long_reads/*.fastq | fastqc -t 3 stdin:long_reads


