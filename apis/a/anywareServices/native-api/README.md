# Anyware Services: Native API Reference

A consolidated summary of Anyware Services's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html
- **API base URL:** `https://demo.ametys.org`

## Authentication

### API Key

Use an Ametys Content IO API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

Responses from this API use XML. Response data is read from `ActionResult`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Import Content At Root](actions/import-content-at-root.md) | `POST /_contentio/import/content/:site/:lang` | [docs](https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html) |
| [Import Content Under Parent Path](actions/import-content-under-parent-path.md) | `POST /_contentio/import/content/:site/:lang/:path` | [docs](https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html) |
