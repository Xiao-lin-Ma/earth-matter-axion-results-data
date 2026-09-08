# Open Results Data for Earth Matter Enhanced Axion Dark Matter Search

This repository provides the open numerical results associated with
[arXiv:2602.20260](https://arxiv.org/abs/2602.20260), *Earth Matter Enhanced
Axion Dark Matter Search*. It contains the final pointwise 95% upper limits used
as the inputs to the Earth-enhanced and standard-halo-model (SHM) result curves
in Figure 3.

## Data sets

- `earth_enhanced/`: Earth-enhanced pointwise limits.
- `standard_halo_shm/`: standard-halo pointwise limits.

Each data set contains 7,755,154 frequency points spanning 0.01 Hz to
approximately 7 Hz.

Each CSV has exactly two columns:

| Column | Description | Unit |
| --- | --- | --- |
| `frequency_Hz` | Axion Compton frequency, $m_a/(2\pi)$ | Hz |
| `coupling_95CL_GeV^-1` | Pointwise 95% upper limit on $g_{an}$ | GeV$^{-1}$ |

## Integrity check

`SHA256SUMS` contains a SHA-256 checksum for every CSV part. From the repository
root, verify all files with:

```bash
shasum -a 256 -c SHA256SUMS
```
