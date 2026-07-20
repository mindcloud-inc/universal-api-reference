# DocRaptor: Native API Reference

A consolidated summary of DocRaptor's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docraptor.com/documentation/api/making_documents
- **API base URL:** `https://api.docraptor.com`

## Authentication

### API Key

Authenticate with DocRaptor HTTP Basic auth using the DocRaptor API key as the username and a blank password.

### Credentials

- **DocRaptor API key:** `username` · required
- **Password (leave blank):** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docraptor.com/documentation/api/making_documents)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Async PDF from HTML Content](actions/create-async-pdf-from-html-content.md) | `POST /docs` | [docs](https://docraptor.com/documentation/api/async) |
| [Create PDF from HTML Content](actions/create-pdf-from-html-content.md) | `POST /docs` | [docs](https://docraptor.com/documentation/api/making_documents) |
| [Create PDF from URL](actions/create-pdf-from-url.md) | `POST /docs` | [docs](https://docraptor.com/documentation/api/making_documents) |
| [Create XLSX from HTML Content](actions/create-xlsx-from-html-content.md) | `POST /docs` | [docs](https://docraptor.com/documentation/api/making_documents) |
| [Get Async Document Status](actions/get-async-document-status.md) | `GET https://docraptor.com/status/:status_id` | [docs](https://docraptor.com/documentation/api/async) |
| [List DocRaptor IP Addresses](actions/list-docraptor-ip-addresses.md) | `GET https://docraptor.com/ips.json` | [docs](https://docraptor.com/documentation/api/ip_listing) |
| [List Documents](actions/list-documents.md) | `GET /docs.json` | [docs](https://docraptor.com/documentation/api/document_listing) |
