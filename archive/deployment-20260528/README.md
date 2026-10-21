# Historical deployment material

This archive was recorded on 2026-10-21. The original 51 files from upstream commit
`fb5974ec0f3840ecdd973d20cd74a0735f62289c` remain unchanged in the repository.

- `package-lock.json` is the exact lockfile from the observed deployment
  filesystem. Its SHA-256 is
  `a695adf74bcec29c9387a847a13c90825fb7869b0063f9d892693d2c389859c9`.
  Compared with the upstream lockfile, only the top-level package name and the
  root package name changed from `cashclaw` to `cashclaw-agent`. Dependency
  entries did not change. The other 50 upstream files matched byte for byte.
- `Dockerfile` is a recipe retained from the historical local deployment
  package. Its SHA-256 is
  `522da6990521d1a8e405a84c0c4101ccacf9f3726a260e9ac7a4310d0bc0ca20`.
  It has not been established that this exact file produced the observed image.

The recipe uses an unpinned base image, upstream branch, and global CLI install.
It is retained for provenance and has not been rebuilt or executed during the
retirement. A reproducible reconstruction has not been demonstrated.

Credentials, environment files, runtime state, and private recovery evidence are
not part of this public archive. Any future activation requires operator approval
and a new configuration and security review.
