# M. tuberculosis WGS Variant Analysis Workflow

Galaxy-based whole-genome sequencing workflow for analysing *Mycobacterium tuberculosis* short-read data, with a focus on resistance-associated variant detection and interpretation.

## Overview

This project contains a Galaxy workflow developed for end-to-end WGS analysis of *M. tuberculosis* isolates. The workflow covers sequence retrieval, quality control, trimming, alignment, BAM processing, coverage assessment, variant calling, filtering, annotation, and reporting.

It was designed to support reproducible analysis of resistance-associated loci using standard bioinformatics tools in a workflow-based environment.

## Objectives

- Perform reproducible WGS analysis of *M. tuberculosis* short-read datasets
- Assess sequencing quality and alignment performance
- Identify and annotate variants in resistance-associated loci
- Support interpretation using coverage metrics, variant statistics, and IGV inspection

## Workflow Steps

1. FASTQ retrieval using `fasterq-dump`
2. Quality control using `Falco`
3. Read trimming using `fastp` and `Cutadapt`
4. Alignment to reference genome using `BWA-MEM2`
5. BAM sorting and duplicate marking using `Picard`
6. Mapping QC using `Samtools flagstat` and `idxstats`
7. Coverage analysis using `mosdepth`
8. Variant calling and filtering using `bcftools`
9. Variant annotation using `bcftools csq`, `SnpEff`, and `SnpSift`
10. Aggregate reporting using `MultiQC`
11. Read-level review in `IGV`

## Tools Used

`Galaxy`, `fasterq-dump`, `Falco`, `fastp`, `Cutadapt`, `BWA-MEM2`, `Picard`, `Samtools`, `mosdepth`, `bcftools`, `SnpEff`, `SnpSift`, `MultiQC`, `IGV`

## Outputs

- QC and trimming summary
- Mapping summary
- Variant tables for resistance-associated loci
- Resistance interpretation summary
- IGV screenshots for selected mutations

## Key Skills Demonstrated

- NGS workflow design
- WGS variant calling
- QC and coverage assessment
- Variant annotation and interpretation
- Reproducible bioinformatics analysis
- Galaxy-based workflow development

## Notes

This repository is intended as a portfolio project demonstrating applied bioinformatics workflow development and interpretation in a genomics context.
