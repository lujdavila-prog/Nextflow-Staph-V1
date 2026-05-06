# Nextflow-Staph-V1
This pipeline is designed to assess whether selected samples accurately match a S. aureus reference genome. A high mapping rate indicates the sample is S. aureus or a closely related strain, while a low mapping rate suggests the sample may represent a highly divergent or mutated strain, or an entirely different organism.

The pipeline uses Docker containers with FASTP to quality-filter and trim raw reads, BWA to generate a reference index and align the sample to that index, and SAMtools to sort and index the resulting alignment, producing a BAM file and a flagstat report summarizing mapping statistics.

This pipeline was specifically built for SRR37176627, a publicly available S. aureus accession from the NCBI Sequence Read Archive. It will work for other FASTQ.gz files as long as params.reads and params.genome are updated accordingly in the script.

Nextflow and Docker are required to run this pipeline.
