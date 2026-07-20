# PDF Snake: Native API Reference

A consolidated summary of PDF Snake's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.pdfsnake.com/tutorials/web-api.html
- **OpenAPI specification:** https://api.swaggerhub.com/apis/R7274/PDFSnakeWebApi/6.227.0?resolved=true
- **API base URL:** `https://api2.pdfsnake.app/api/v2`

## Authentication

### API Key

Use a PDF Snake API key from https://pdfsnake.app/api. The provider accepts it as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.pdfsnake.com/tutorials/web-api.html)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Byte Balance](actions/get-byte-balance.md) | `POST /balance` | [docs](https://api.swaggerhub.com/apis/R7274/PDFSnakeWebApi/6.227.0?resolved=true) |
| [Impose Document](actions/impose-document.md) | `POST /impose` | [docs](https://api.swaggerhub.com/apis/R7274/PDFSnakeWebApi/6.227.0?resolved=true) |
