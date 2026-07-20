# DSCO Dropship EDI: Native API Reference

A consolidated summary of DSCO Dropship EDI's API configuration, with links to official documentation.

- **Official docs:** https://developer.dsco.io/reference/introduction

## Authentication

### SFTP Credentials

Tenant-specific DSCO SFTP credentials.

### Credentials

- **Host:** `host` · required · DSCO tenant SFTP hostname.
- **Port:** `port` · optional · SFTP port. DSCO uses 22.
- **Username:** `username` · required · DSCO tenant SFTP username.
- **Password:** `password` · required · DSCO tenant SFTP password.
- **Use SFTP:** `useSftp` · optional · Keep enabled for DSCO Dropship EDI connections.

[Official authentication documentation](https://developer.dsco.io/reference/introduction)
