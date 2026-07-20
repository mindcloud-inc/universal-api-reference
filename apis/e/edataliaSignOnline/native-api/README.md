# edatalia Sign Online: Native API Reference

A consolidated summary of edatalia Sign Online's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://edatalia.com/kb/api-rest-40/
- **OpenAPI specification:** https://restapi.firmar.online/index.html
- **API base URL:** `https://restapi.firmar.online`

## Authentication

### API Key

Use an edatalia firmar.online API key from the production or sandbox web app. The API declares the Authorization header as the API key/JWT bearer token location.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://edatalia.com/kb/api-rest-40/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Envelope Audit Trail](actions/get-envelope-audit-trail.md) | `GET /PSC/v40/DocumentSet/AuditTrail/:documentSetId` | [docs](https://restapi.firmar.online/index.html) |
| [Get Envelope Details](actions/get-envelope-details.md) | `GET /PSC/v40/DocumentSet/:documentSetId` | [docs](https://restapi.firmar.online/index.html) |
| [Get Envelope Evidence Document](actions/get-envelope-evidence-document.md) | `GET /PSC/v40/DocumentSet/Evidences/:documentSetId` | [docs](https://restapi.firmar.online/index.html) |
| [Get Envelope Signing URL](actions/get-envelope-signing-url.md) | `GET /PSC/v40/DocumentSet/Url/:documentSetId` | [docs](https://restapi.firmar.online/index.html) |
| [Get Envelope Status](actions/get-envelope-status.md) | `GET /PSC/v40/DocumentSet/Status/:documentSetId` | [docs](https://restapi.firmar.online/index.html) |
| [List Devices](actions/list-devices.md) | `GET /PSC/v40/Device` | [docs](https://restapi.firmar.online/index.html) |
| [List Signature History](actions/list-signature-history.md) | `GET /PSC/v40/History` | [docs](https://restapi.firmar.online/index.html) |
| [Search Envelopes By Reference](actions/search-envelopes-by-reference.md) | `GET /PSC/v40/DocumentSet/InfoByReference/:documentSetReference` | [docs](https://restapi.firmar.online/index.html) |
| [Sign PDF With Certificate](actions/sign-pdf-with-certificate.md) | `POST /eSign/v40/Signature` | [docs](https://restapi.firmar.online/index.html) |
| [Timestamp Signed PDF](actions/timestamp-signed-pdf.md) | `POST /eSign/v40/Signature/Timestamp` | [docs](https://restapi.firmar.online/index.html) |
