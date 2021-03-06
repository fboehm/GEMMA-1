## ChangeLog v0.97 (2017/12/19)

This is a massive bug fix release with many improvements. For contributions
see
[contributors](https://github.com/genetics-statistics/GEMMA/graphs/contributors)
and
[commits](https://github.com/genetics-statistics/GEMMA/commits/master).

### Speedup of GEMMA by using optimized OpenBlas

* Providing a binary release with OpenBlas optimization for Intel Haswell
* Dropped using standar lapack and gslcblas libs
* Fixed NaN bug with GSL2 and made recent libraries the default
* Minimized use of Eigenlib libraries (single threaded and slow compilation)
* -legacy switch provides v0.96 behaviour (incl. eigenlib)

### Added Leave One Chromosome Out (LOCO) support for Bimbam (K and LMM)

* See 449d882a3b33ef81ef4f0127c3932b01fa796dbb
* -snps [filename] option allow selecting a subset of SNPs for analysis
* -loco [chr] option for K and LMM computations
* added [gemma-wrapper](https://github.com/genetics-statistics/gemma-wrapper) to make using LOCO easy
* LOCO examples in https://github.com/genetics-statistics/GEMMA/blob/master/test/dev_test_suite.sh

### Added checks for matrices

* #72 and #45 implements
  1. Fail if K has negative eigen values
  2. Fail if K is not symmetric
  3. Fail if K is not positive definite
  4. Warn in eigen values are very small
  5. Warn if K is ill conditioned
* Check for NaN values

### Added test framework and unit tests

* Added integration and unit tests, as well as
  [Travis-CI](https://travis-ci.org/genenetwork/GEMMA) support
* Improved debug information and testing of input files

### Other

* #81 printing out beta and se(beta) under -lmm 2 as well as logl_H1
* Improved README and INSTALL docs
* Added support info and code of conduct
* Reformatted the full source tree with 3935ba39d30666dd7d4a831155631847c77b70c4
* Merged LMM computation for Plink and Bimbam formats
* Fixed progressbar issues
* #46 removed support for Oxford format
* Got rid of all compiler warnings
* Updated copyright banner, info and license information for included software
* Started a [discussion list](https://groups.google.com/forum/#!forum/gemma-discussion)

See also [commits](https://github.com/genetics-statistics/GEMMA/commits/master).

## GEMMA 0.96.0

+ First stable release.

## GEMMA 0.95.2

+ Resolved Issue #36.

## GEMMA 0.95.1

+ Created first release of GEMMA 0.95a following request in Issue #33.

## GEMMA 0.94.1

+ Fixed a bug (the predict option for multiple phenotype imputation
was not recoginzed with PLINK files).

## GEMMA 0.94.0

+ Implemented the multivariate linear mixed model.

## GEMMA 0.93

+ Implemented the Bayesian sparse linear mixed model.

## GEMMA 0.92

+ Fixed a few typos.

+ Now allows for missing values in the covariates file.

+ Included REMLE estimate for lambda in the output .log file.

+ Added small GWAS example dataset

+ Added detailed user manual.

## GEMMA 0.91

+ Fixed a bug (BIMBAM annotation file not recognized).

## GEMMA 0.90

+ Initial pre-release.

See also https://github.com/genetics-statistics/GEMMA/releases
