# Samtools

This is a singularity image to deploy samtools.

This will produce a Singularity image (suitable for running in a cluster environment) using [https://hub.docker.com/r/broadinstitute/picard/](https://hub.docker.com/r/broadinstitute/picard/). We do this by way of a bootstrap file for the Docker image.


## 1. Install Singularity

Instructions can be found on the [singularity site](https://singularityware.github.io).


## 2. Bootstrap the image


    sudo singularity create --size 4000 samtools.img
    sudo singularity bootstrap samtools.img Singularity


## 3. Run commands

How to access the samtools runtime executable?


       ./samtools.img

	Program: samtools (Tools for alignments in the SAM format)
	Version: 1.3.1 (using htslib 1.3.1)

	Usage:   samtools <command> [options]

	Commands:
	  -- Indexing
	     dict           create a sequence dictionary file
	     faidx          index/extract FASTA
	     index          index alignment

	  -- Editing
	     calmd          recalculate MD/NM tags and '=' bases
	     fixmate        fix mate information
	     reheader       replace BAM header
	     rmdup          remove PCR duplicates
	     targetcut      cut fosmid regions (for fosmid pool only)
	     addreplacerg   adds or replaces RG tags

	  -- File operations
	     collate        shuffle and group alignments by name
	     cat            concatenate BAMs
	     merge          merge sorted alignments
	     mpileup        multi-way pileup
	     sort           sort alignment file
	     split          splits a file by read group
	     quickcheck     quickly check if SAM/BAM/CRAM file appears intact
	     fastq          converts a BAM to a FASTQ
	     fasta          converts a BAM to a FASTA

	  -- Statistics
	     bedcov         read depth per BED region
	     depth          compute the depth
	     flagstat       simple stats
	     idxstats       BAM index stats
	     phase          phase heterozygotes
	     stats          generate stats (former bamcheck)

	  -- Viewing
	     flags          explain BAM flags
	     tview          text alignment viewer
	     view           SAM<->BAM<->CRAM conversion
	     depad          convert padded BAM to unpadded BAM


