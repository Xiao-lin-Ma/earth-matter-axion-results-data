# Open Results Data for Earth Matter Enhanced Axion Dark Matter Search

This repository provides the open numerical results associated with
[arXiv:2602.20260](https://arxiv.org/abs/2602.20260), *Earth Matter Enhanced
Axion Dark Matter Search*. It contains the final pointwise 95% upper limits used
as the inputs to the Earth-enhanced and standard-halo-model (SHM) result curves
in Figure 3. Only the frequency and axion-neutron coupling limit are included.

The release does not contain time-series data, power spectral densities,
best-fit couplings, significances, background constraints, or intermediate
likelihood outputs.

## Data sets

- `earth_enhanced/`: Earth-enhanced pointwise limits.
- `standard_halo_shm/`: standard-halo pointwise limits.

Each data set contains 7,755,154 frequency points spanning 0.01 Hz to
approximately 7 Hz. To keep individual files suitable for ordinary GitHub
storage, each table is divided into eight consecutive, frequency-ordered CSV
parts. The first seven parts contain 1,000,000 rows each and the final part
contains 755,154 rows.

Concatenate or load the parts in filename order to reconstruct the complete
table. Each CSV has exactly two columns:

| Column | Description | Unit |
| --- | --- | --- |
| `frequency_Hz` | Axion Compton frequency, $m_a/(2\pi)$ | Hz |
| `coupling_95CL_GeV^-1` | Pointwise 95% upper limit on $|g_{an}|$ | GeV$^{-1}$ |

The published plotting lines may use local frequency averaging for visual
clarity. The CSV files retain the final pointwise 95% limits immediately before
that display-only averaging step.

## Integrity check

`SHA256SUMS` contains a SHA-256 checksum for every CSV part. From the repository
root, verify all files with:

```bash
shasum -a 256 -c SHA256SUMS
```
