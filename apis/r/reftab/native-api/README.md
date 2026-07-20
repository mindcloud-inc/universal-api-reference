# Reftab: Native API Reference

A consolidated summary of Reftab's API configuration, with links to official documentation.

- **Official docs:** https://www.reftab.com/api-docs/
- **OpenAPI specification:** https://prod.0codekit.com/openapi.json
- **API base URL:** `https://www.reftab.com`

## Authentication

### Signed Request

Use a Reftab public key and secret key to sign each request.

### Credentials

- **Public Key:** `publicKey` · required · Reftab API public key from Settings > API Keys.
- **Secret Key:** `secretKey` · required · Reftab API secret key from Settings > API Keys.

[Official authentication documentation](https://www.reftab.com/faq/postman-reftab-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
