# Tenderplan: Native API Reference

A consolidated summary of Tenderplan's API configuration, with links to official documentation.

- **Official docs:** https://tenderplan.ru/api/doc/
- **OpenAPI specification:** https://tenderplan.ru/api/doc/app.baf92e31bbaa7955042b.bundle.js
- **API base URL:** `https://tenderplan.ru`

## Authentication

### API Key

Use a Tenderplan access token or personal access token. Requests are sent with Authorization: Bearer using the stored API key credential.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tenderplan.ru/api/doc/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.
