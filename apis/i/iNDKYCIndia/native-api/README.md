# IN-D KYC India: Native API Reference

A consolidated summary of IN-D KYC India's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://dev.in-d.ai/
- **API base URL:** `https://api.kyc.in-d.ai`

## Authentication

### API Key

Authenticate requests with the IN-D KYC x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/indkycindia/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Face Liveness](actions/check-face-liveness.md) | `POST /api/facelivenessv2/` | [docs](https://dev.in-d.ai/api-documentation/#operation/faceliveness_id) |
| [Check Face Liveness For UID](actions/check-face-liveness-for-uid.md) | `POST /api/facelivenessv2/{uid}` | [docs](https://dev.in-d.ai/api-documentation/#operation/faceliveness_uid) |
| [Check Video Liveness](actions/check-video-liveness.md) | `POST /api/liveliness/` | [docs](https://dev.in-d.ai/api-documentation/#operation/videoliveliness_id) |
| [Check Video Liveness For UID](actions/check-video-liveness-for-uid.md) | `POST /api/liveliness/{uid}` | [docs](https://dev.in-d.ai/api-documentation/#operation/videoliveliness_uid) |
| [Classify ID Document](actions/classify-id-document.md) | `POST /api/mw/classification` | [docs](https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/certified-connectors/IN-D%20KYC-India/apiDefinition.swagger.json) |
| [Classify ID Documents](actions/classify-id-documents.md) | `POST /api/class/` | [docs](https://dev.in-d.ai/api-documentation/#operation/classify_id) |
| [Classify ID Documents For UID](actions/classify-id-documents-for-uid.md) | `POST /api/class/{uid}` | [docs](https://dev.in-d.ai/api-documentation/#operation/classify1_id) |
| [Extract ID Fields](actions/extract-id-fields.md) | `POST /api/fields/` | [docs](https://dev.in-d.ai/api-documentation/#operation/extract_id) |
| [Extract ID Fields For UID](actions/extract-id-fields-for-uid.md) | `POST /api/fields/{uid}` | [docs](https://dev.in-d.ai/api-documentation/#operation/extract1_id) |
| [Generate UID](actions/generate-uid.md) | `GET /api/upload/uid` | [docs](https://dev.in-d.ai/api-documentation/#operation/generate_uid_id) |
| [Get Connector Documentation](actions/get-connector-documentation.md) | `GET https://learn.microsoft.com/en-us/connectors/indkycindia/` | [docs](https://learn.microsoft.com/en-us/connectors/indkycindia/) |
| [Match Faces](actions/match-faces.md) | `POST /api/facematch/` | [docs](https://dev.in-d.ai/api-documentation/#operation/facematch_id) |
| [Match Faces For UID](actions/match-faces-for-uid.md) | `POST /api/facematch/{uid}` | [docs](https://dev.in-d.ai/api-documentation/#operation/facematch_uid) |
| [Validate ID Number](actions/validate-id-number.md) | `POST /api/validation/` | [docs](https://dev.in-d.ai/api-documentation/#operation/validate_id) |
| [Validate ID Number For UID](actions/validate-id-number-for-uid.md) | `POST /api/validation/{uid}` | [docs](https://dev.in-d.ai/api-documentation/#operation/validate1_id) |
