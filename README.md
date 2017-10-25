# Awesome TCGA [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Curated list of awesome resources to access data from The Cancer Genome Atlas (TCGA) project, with a particular focus on computational tools allowing pan-TCGA analysis and/or giving access to the results of such tools.

## Official links

### General informations

- [TCGA project homepage](https://cancergenome.nih.gov)
- [Infographic summary of the project](https://cancergenome.nih.gov/PublishedContent/Images/images/tcga-infographic-enlarge.__v100169753.png)
- [Data documentation](https://docs.gdc.cancer.gov/Data/Introduction/) - Describe how the data is generated, in particular the details of the bioinformatics pipeline used.

### Data repositories

- [Genomic Data Commons (GDC) data portal](https://portal.gdc.cancer.gov) - The old TCGA data portal (https://tcga-data.nci.nih.gov/docs/publications/tcga/) is no longer operational and all TCGA data now resides at the GDC. Note that the GDC host other datasets than just the TCGA.
- [GDC homepage](https://portal.gdc.cancer.gov)
- [GDC data documentation](https://docs.gdc.cancer.gov)
- [GDC data release notes](https://docs.gdc.cancer.gov/Data/Release_Notes/Data_Release_Notes/)
- [GDC legacy archive](https://portal.gdc.cancer.gov/legacy-archive/) - The legacy data is the original data that uses the old genome build (hg19) as produced by the original submitter. The legacy data is not actively being updated in any way. Users should migrate to the harmonized data.
- [List of cohorts with sample sizes](https://portal.gdc.cancer.gov/projects?filters=~%28op~%27and~content~%28~%28op~%27in~content~%28field~%27projects.program.name~value~%28~%27TCGA%29%29%29%29%29) - Shortcut to the GDC data portal with the list of all cancer sites with the number of cases and the number of available cases per data category.

## Downloading the data

List of command line tools, API or R packages to download the data.

### Official tools

- [GDC data transfert tool](https://gdc.cancer.gov/access-data/gdc-data-transfer-tool) - Official command line tool, see [here](https://github.com/IARCbioinfo/GDC-tricks) for a nice tutorial.
- [GDC API](https://docs.gdc.cancer.gov/API/Users_Guide/Getting_Started/) - Official HTTP API. Note the [BAM Slicing](https://docs.gdc.cancer.gov/API/Users_Guide/BAM_Slicing/) that can be quite useful.

### Broad Institute GDAC

The Broad TCGA Data and Analyses (Broad GDAC) Firehose provides TCGA Level 3 data and Level 4 analyses packaged in a form amenable to immediate algorithmic analysis. This is a useful resource to access analyses results not performed by the GDC (e.g. MutSig2CV, correlation with clinical variables, mRNA clustering etc.). They are automatically running in a systematic way the software we usually see in a TCGA publication. However the data is currently based on the old hg19 TCGA data for somatic variant calling.

- [Firehose](http://gdac.broadinstitute.org/) - Refers to the computational infrastructure.
    - [Python and UNIX wrappers](https://confluence.broadinstitute.org/display/GDAC/fbget)
    - [FirebrowseR](https://github.com/mariodeng/FirebrowseR) - An R package to download directly the results of the analyses performed by Firehose in R.
- [Firebrowse](http://firebrowse.org) - A web UI to visualise the results of the analyses performed by Firehose.

### Others

The GDC hosts a list of such tools: https://gdc.cancer.gov/access-data/gdc-community-tools.

- [TCGABiolinks](http://bioinformaticsfmrp.github.io/TCGAbiolinks/) - A R/Bioconductor package to search, download and prepare relevant data for analysis in R. Very powerful and well documented.
- [GDC Spreadsheet Download Tool](https://github.com/wwysoc2/gdc-tsv-tool) - Tool to download clinical and/or biospecimen metadata for a given set of files in a tab-delimited format.
- [GenomicDataCommons](https://bioconductor.org/packages/release/bioc/html/GenomicDataCommons.html) - A R/Bioconductor package for querying, accessing, and mining genomic datasets available from the GDC.
- [gdctools](https://github.com/broadinstitute/gdctools) - Broad Institute Python and UNIX CLI utilities to simplify search and retrieval of open-access data from the GDC.

## Cloud computing

List of cloud computing facilities hosting the TCGA data.

- [Cancer Genomics Cloud](http://www.cancergenomicscloud.org) - Developed by [Seven Bridges Genomics](https://www.sevenbridges.com). They have a [blog](https://www.sevenbridges.com/blog/) with useful case studies.
- [ISB Cancer Genomics Cloud](http://cgc.systemsbiology.net) - Developed by the Institute for Systems Biology in Seattle.
- [FireCloud](https://software.broadinstitute.org/firecloud/) - Developed by the BROAD Institute.

## Pan-TCGA analyses

List of analyses performed in a consistent manner on all (or at least several) TCGA datasets, where the results are freely available.

- [Firehose](http://gdac.broadinstitute.org) - See [above](https://github.com/IARCbioinfo/awesome-TCGA#broad-institute-gdac) for the associated tools to download the data. They run many software on all TCGA cohorts and make the results available.
- [Tumor Fusion Gene Data Portal](http://www.tumorfusions.org) - 9,966 tumor samples from 33 TCGA cancer types and 689 normal samples in 19 TCGA normal tissue types were analyzed by PRADA pipeline and the realigned BAM files of RNAseq data.
- [DriverDBv2](http://driverdb.tms.cmu.edu.tw/driverdbv2/index.php) - WES and RNA-seq reanalysis to identify driver genes. Provides a nice graphical summary of mutation clustering in genes (e.g. for *[TP53](http://driverdb.tms.cmu.edu.tw/driverdbv2/gene_data_p.php?genename=TP53&geneproteinid=&submit=submit)*).
- [ChimerDB](ercsb.ewha.ac.kr/fusiongene) - A comprehensive database of fusion genes encompassing analysis of deep sequencing data (including TCGA) and manual curations.
- [ASCAT Ploidy and Purity Estimates](http://cancer.sanger.ac.uk/cosmic/download) - [COSMIC](http://cancer.sanger.ac.uk/cosmic) hosts a tab separated table listing the ploidy and aberrant cell fraction (purity estimate), for TCGA samples re-analysed using ASCAT.
- [BioXpress](https://hive.biochemistry.gwu.edu/cgi-bin/prd/bioxpress/servlet.cgi). - RNA-seq-derived gene expression database, including TCGA among others.

## Publications

- [Official publication list](https://cancergenome.nih.gov/publications)
- [Publication from Seven Bridges Genomics](https://www.sevenbridges.com/publications/) using their cloud solution.
- [TCGABiolinks](https://www.ncbi.nlm.nih.gov/pubmed/26704973) - Paper describing the R TCGABiolinks package.
- [FirebrowseR](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5216271/) - Paper describing the R FirebrowseR package.
- [GenomicDataCommons](https://www.biorxiv.org/content/early/2017/03/15/117200) -  Paper describing the R GenomicDataCommons package.
- [DriverDBv2](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4702919/)
- [ChimerDB](https://www.ncbi.nlm.nih.gov/pubmed/19906715) - A new paper is in press for v3.0 according to rcsb.ewha.ac.kr/fusiongene.
- [BioXpress](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4377087/).
