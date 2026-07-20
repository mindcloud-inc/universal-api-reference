# Upload to URL: Native API Reference

A consolidated summary of Upload to URL's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://uploadtourl.com/api-docs
- **API base URL:** `https://uploadtourl.com`

## Authentication

### API Key

Authenticate with Upload to URL API using the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://uploadtourl.com/api-docs)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | `DELETE /api/file/:file_id` | [docs](https://uploadtourl.com/api-docs) |
| [Get File Information](actions/get-file-information.md) | `GET /api/file/:file_id` | [docs](https://uploadtourl.com/api-docs) |
| [Publish HTML](actions/publish-html.md) | `POST /api/publish` | [docs](https://uploadtourl.com/api-docs) |
| [Upload File](actions/upload-file.md) | `POST /api/upload` | [docs](https://uploadtourl.com/api-docs) |
