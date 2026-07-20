# PyPI: Native API Reference

A consolidated summary of PyPI's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.pypi.org/api/
- **API base URL:** `https://pypi.org`

## Authentication

### Public API

PyPI's public JSON, Index, Integrity, and Stats APIs do not require authentication for read access.

This API does not require request authentication.

[Official authentication documentation](https://docs.pypi.org/api/)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get File Provenance](actions/get-file-provenance.md) | `GET /integrity/:project/:version/:filename/provenance` | [docs](https://docs.pypi.org/api/integrity/) |
| [Get Project Files Index](actions/get-project-files-index.md) | `GET /simple/:project/` | [docs](https://docs.pypi.org/api/index-api/) |
| [Get Project Metadata](actions/get-project-metadata.md) | `GET /pypi/:project/json` | [docs](https://docs.pypi.org/api/json/) |
| [Get PyPI Stats](actions/get-py-pi-stats.md) | `GET /stats/` | [docs](https://docs.pypi.org/api/stats/) |
| [Get Release Metadata](actions/get-release-metadata.md) | `GET /pypi/:project/:version/json` | [docs](https://docs.pypi.org/api/json/) |
