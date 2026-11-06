# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py bs <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 11,183 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
66d2d526d83bbfc68ec91f4274da7b9292739c1dd5025eae5f28aef3852e6162 *bs_appellationsgericht.parquet
7caf913b4f062e3ab4747a8ad712f06d32b13a8fb4e8f90ccd656d92824fbcf9 *bs_gerichte.parquet
51124566991e5176f8d0a25e880029b6edbf73445fccd37fdbe7aad35566e1ad *bs_personalrekurskommission.parquet
4692bc6058f658ae523e718ce7f5aec95e36e544b0a4e7d8457ab8b37a9f44eb *bs_sozialversicherungsgericht.parquet
667ea0859e073d78de49b07db2f5114c9cf8fafe9b82b4213530aea27785a516 *bs_steuerrekurskommission.parquet
e236f5b384d263e1c145843d2db0ea83e3c82e440da34ab1aa518122863c395c *bs_zivilgericht.parquet
```
