# PDF Maker: Native API Reference

A consolidated summary of PDF Maker's API configuration, with links to official documentation.

- **Official docs:** https://help.thepdfmaker.com/en
- **API base URL:** `https://api.thepdfmaker.com`

## Authentication

### API Key

Use your PDF Maker API key to generate PDFs via the public API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.thepdfmaker.com/en/articles/10850153-how-to-create-professional-pdf-documents-using-pdf-maker-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
