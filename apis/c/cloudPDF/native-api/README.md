# CloudPDF: Native API Reference

A consolidated summary of CloudPDF's API configuration, with links to official documentation.

- **Official docs:** https://cloudpdf.io/developers/api-docs
- **API base URL:** `https://api.cloudpdf.io`

## Authentication

### Simple API Key

Use the CloudPDF Simple API Key in the X-Authorization header. Do not use the Secret Signing Key for this auth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Authorization: <apiKey>
```

[Official authentication documentation](https://cloudpdf.io/developers/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
