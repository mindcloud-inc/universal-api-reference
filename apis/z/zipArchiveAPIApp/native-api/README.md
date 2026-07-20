# Zip Archive API app: Native API Reference

A consolidated summary of Zip Archive API app's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://archiveapi.com/rest-api/
- **API base URL:** `https://api.archiveapi.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.archiveapi.com/rest-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create ZIP Archive](actions/create-zip-archive.md) | `POST /zip` | [docs](https://archiveapi.com/rest-api/file-compression/) |
| [Extract ZIP Archive](actions/extract-zip-archive.md) | `POST /extract` | [docs](https://archiveapi.com/rest-api/archive-extraction/) |
