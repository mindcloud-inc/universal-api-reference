# Ainoflow Convert: Native API Reference

A consolidated summary of Ainoflow Convert's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.ainoflow.io/docs/api/convert
- **API base URL:** `https://api.ainoflow.io`

## Authentication

### API Key

Bearer API key for Ainoflow Convert.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ainoflow.io/docs/api)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Job Status](actions/get-job-status.md) | `GET /api/v1/convert/jobs/:jobId` | [docs](https://www.ainoflow.io/docs/api/convert) |
| [Submit Base64 Document](actions/submit-base64-document.md) | `POST /api/v1/convert/submit-base64` | [docs](https://www.ainoflow.io/docs/api/convert) |
| [Submit External URL](actions/submit-external-url.md) | `POST /api/v1/convert/submit-url` | [docs](https://www.ainoflow.io/docs/api/convert) |
| [Submit File for Processing](actions/submit-file-for-processing.md) | `POST /api/v1/convert/submit-file` | [docs](https://www.ainoflow.io/docs/api/convert) |
