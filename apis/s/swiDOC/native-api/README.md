# swiDOC: Native API Reference

A consolidated summary of swiDOC's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://api.docs.swidoc.ch/swagger.yml
- **OpenAPI specification:** https://api.docs.swidoc.ch/swagger.yml
- **API base URL:** `https://app.swidoc.ch/api/v1`

## Authentication

### API Key

Authenticate requests with the swiDOC API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.docs.swidoc.ch/swagger.yml)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Document](actions/archive-document.md) | `POST /documents` | [docs](https://api.docs.swidoc.ch/swagger.yml) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://api.docs.swidoc.ch/swagger.yml) |
| [Get Document Metadata](actions/get-document-metadata.md) | `GET /documents/:documentId/metadata` | [docs](https://api.docs.swidoc.ch/swagger.yml) |
| [Update Document Metadata](actions/update-document-metadata.md) | `PATCH /documents/:documentId/metadata` | [docs](https://api.docs.swidoc.ch/swagger.yml) |
