# DigiSigner: Native API Reference

A consolidated summary of DigiSigner's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.digisigner.com/esignature-api/esignature-api-documentation/
- **API base URL:** `https://api.digisigner.com/v1`

## Authentication

### API Key

Authenticate with your DigiSigner API key. Requests send it using DigiSigner's documented Basic header format.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## API conventions

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:documentId` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
| [Download Document](actions/download-document.md) | `GET /documents/:documentId` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
| [Download Document Attachment](actions/download-document-attachment.md) | `GET /documents/:documentId/fields/:fieldApiId/attachment` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
| [Get Document Fields](actions/get-document-fields.md) | `GET /documents/:documentId/fields` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
| [Get Signature Request Status](actions/get-signature-request-status.md) | `GET /signature_requests/:signatureRequestId` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
| [Send Signature Request](actions/send-signature-request.md) | `POST /signature_requests` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
| [Upload Document](actions/upload-document.md) | `POST /documents` | [docs](https://www.digisigner.com/esignature-api/esignature-api-documentation/) |
