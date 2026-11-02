# Harmonize two independent sumstats against an LD reference

Used for valid inference where discovery weights (`w`) and target
Z-scores (`Z`) must come from independent cohorts.

## Usage

``` r
harmonize_two(disc, targ, bim, ld, freq_tol = 0.15)
```

## Arguments

- disc:

  Discovery sumstats (provides weights `w`).

- targ:

  Target sumstats (provides Z-scores `Z`).

- bim:

  Output of
  [`read_bim`](https://github.com/shan-team/RAS_GWAS_Summary/reference/read_bim.md).

- ld:

  Output of
  [`ld_matrix`](https://github.com/shan-team/RAS_GWAS_Summary/reference/ld_matrix.md).

- freq_tol:

  Maximum \|EAF - reference frequency\| tolerance.

## Value

List with w, Z, bp, R, ids, n_kept, all aligned to each other.
