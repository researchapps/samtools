# BCFTools

This is a singularity image to deploy bcftools.

This will produce a Singularity image (suitable for running in a cluster environment) using [https://hub.docker.com/r/broadinstitute/picard/](https://hub.docker.com/r/broadinstitute/picard/). We do this by way of a bootstrap file for the Docker image.


## 1. Install Singularity

Instructions can be found on the [singularity site](https://singularityware.github.io).


## 2. Bootstrap the image


    sudo singularity create --size 4000 bcftools.img
    sudo singularity bootstrap bcftools.img Singularity


## 3. Run commands

How to access the bcftools runtime executable?


       ./bcftools.img

	Program: bcftools (Tools for variant calling and manipulating VCFs and BCFs)
	Version: 1.3.1 (using htslib 1.3.1)

	Usage:   bcftools [--version|--version-only] [--help] <command> <argument>

	Commands:

	 -- Indexing
	    index        index VCF/BCF files

	 -- VCF/BCF manipulation
	    annotate     annotate and edit VCF/BCF files
	    concat       concatenate VCF/BCF files from the same set of samples
	    convert      convert VCF/BCF files to different formats and back
	    isec         intersections of VCF/BCF files
	    merge        merge VCF/BCF files files from non-overlapping sample sets
	    norm         left-align and normalize indels
	    plugin       user-defined plugins
	    query        transform VCF/BCF into user-defined formats
	    reheader     modify VCF/BCF header, change sample names
	    view         VCF/BCF conversion, view, subset and filter VCF/BCF files

	 -- VCF/BCF analysis
	    call         SNP/indel calling
	    consensus    create consensus sequence by applying VCF variants
	    cnv          HMM CNV calling
	    filter       filter VCF/BCF files using fixed thresholds
	    gtcheck      check sample concordance, detect sample swaps and contamination
	    roh          identify runs of autozygosity (HMM)
	    stats        produce VCF/BCF stats

	 Most commands accept VCF, bgzipped VCF, and BCF with the file type detected
	 automatically even when streaming from a pipe. Indexed VCF and BCF will work
	 in all situations. Un-indexed VCF and BCF and streams will work in most but
	 not all situations.


