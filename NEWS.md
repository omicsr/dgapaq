# dgapaq (development version)

# dgapaq 0.7.0

## New feature

* In `R/compress_coverage.R`, 
    + `compress_coverage()` allows to compress coverage file (output of `samtools depth`) into contiguous segments based on position.
* In `R/check_genotype.R`, 
    + `create_genotype_matrix()` allows to create a genotype matrix based on VCFs.
    + `check_genotype()` allows to check missing data in genotype matrix against coverage information.
* In `R/tidy_vcf.R`, 
    + `tidy_vcf()` allows to correct missing genotypes in VCF using corrected genotype matrix (output of `check_genotype()`)
    
## Minor improvements and fixes

* In [rmarkdown templates](inst/rmarkdown/templates),
    + Fix number of duplicated samples in text.
    + Fix descriptive table, to not show duplicates.

# dgapaq 0.6.1

## Minor improvements and fixes

* In [rmarkdown templates](inst/rmarkdown/templates),
    + Fix wrong formula for heterozygosity outliers.

# dgapaq 0.6.0

## New feature

* In `R/convert_assembly.R`, 
    + `convert_assembly()` allows to convert VCFs to target genome assembly 
    using the software [CrossMap](https://crossmap.readthedocs.io/en/latest/).

# dgapaq 0.5.2

* In [rmarkdown templates](inst/rmarkdown/templates),
    + Small refactoring.
    + Ensure FID and IID are of type character.

# dgapaq 0.5.1

* In [rmarkdown templates](inst/rmarkdown/templates),
    + Fix wrong scale in homozygosity figure.
    + Fix typos in homozygosity figure.
    + Fix exclusion list in Excel.

# dgapaq 0.5.0

* In `DESCRIPTION`,
    + Use `Suggests` instead of `Imports`.
* In `R/qc_plink.R`, 
    + Remove imports.
* In `R/qc_vcf.R`, 
    + Remove imports.

# dgapaq 0.4.1

* In [rmarkdown templates](inst/rmarkdown/templates),
    + Reorder code in setup chunk.

# dgapaq 0.4.0

## Major improvements

* In [rmarkdown templates](inst/rmarkdown/templates),
  + Now uses `data.table`.
  + Now uses `gt`.
  + Now uses `ggplot2`.
  + Improved text, figures and tables.
  
* In `R/qc_vcf.R` and `R/qc_plink.R`, 
  + Core update based on new [rmarkdown templates](inst/rmarkdown/templates).

# dgapaq 0.3.0

## Minor improvements and fixes

* In [rmarkdown template](inst/rmarkdown/templates/qc_vcf/skeleton/skeleton.Rmd),
  + Improve performance and memory consumption.
* In `R/qc_vcf.R`, 
  + Update imports based on [rmarkdown template](inst/rmarkdown/templates/qc_vcf/skeleton/skeleton.Rmd).

# dgapaq 0.2.0

## Minor improvements and fixes

* In `DESCRIPTION`, 
  + Remove dependendy to libterm-readkey-perl.
  + Update all packages listed in `Imports`.
  + Now imports `ggplot2 v3.3.0`.
  + Now imports `gt`.
* Add the no read key version of [HRC perl script](inst/perl/HRC-1000G-check-bim-NoReadKey.pl).
* In [rmarkdown template](inst/rmarkdown/templates/qc_vcf/skeleton/skeleton.Rmd),
  + Reorder YAML header in `qc_vcf()`.
  + Fix condition when be files are not available.
  + Fix merge of files after check against reference panel.
  + Fix combined vcf files not created.
  + Fix issue with reference allele.
  + Fix a typos in the names of a parameters.
  + Fix gender check text printed when check was disabled.
  + Fix condition when fasta file is not provided.
  + Ensure missing values are moved before computing mean.
  + Ensure scale for shape has always the right number of values.
  + Add missing new line in summary.
  + Add condition when no fasta file is provided.
* In `R/qc_vcf.R`, 
  + Add filenames and URLs to download needed files.
* In `R/qc_plink.R`, 
  + Fix a typos in the names of a parameters.
  + Now also work on non-binary PLINK files (*i.e.*, `.map` and `.ped`).

# dgapaq 0.1.0

## New features

* `qc_plink()` allows to compute quality-control of genotyping array (PLINK format) 
    using a [rmarkdown template](inst/rmarkdown/templates/qc_plink/skeleton/skeleton.Rmd).
* `qc_vcf()` allows to compute post-imputation quality-control report 
    using a default [rmarkdown template](inst/rmarkdown/templates/qc_vcf/skeleton/skeleton.Rmd).

