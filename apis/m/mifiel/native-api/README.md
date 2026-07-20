# Mifiel: Native API Reference

A consolidated summary of Mifiel's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.mifiel.com/en/
- **OpenAPI specification:** https://docs.mifiel.com/en/api.json
- **API base URL:** `https://app.mifiel.com`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.mifiel.com/es/#tag/Autenticacion/Autenticacion-Basica)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /api/v1/documents` | [docs](https://docs.mifiel.com/en/#tag/Document/operation/CreateDocument) |
| [Create Stakeholder](actions/create-stakeholder.md) | `POST /api/v1/documents/:documentId/stakeholders` | [docs](https://docs.mifiel.com/en/#tag/Stakeholders/operation/CreateStakeholder) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v1/webhooks` | [docs](https://docs.mifiel.com/en/#tag/Webhooks/operation/CreateWebhook) |
| [Delete Document](actions/delete-document.md) | `DELETE /api/v1/documents/:id` | [docs](https://docs.mifiel.com/en/#tag/Document/operation/DeleteDocument) |
| [Delete Stakeholder](actions/delete-stakeholder.md) | `DELETE /api/v1/documents/:documentId/stakeholders/:id` | [docs](https://docs.mifiel.com/en/#tag/Stakeholders/operation/DeleteStakeholder) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v1/webhooks/:id` | [docs](https://docs.mifiel.com/en/#tag/Webhooks/operation/DeleteWebhook) |
| [Download Signed PDF](actions/download-signed-pdf.md) | `GET /api/v1/documents/:id/file_signed` | [docs](https://docs.mifiel.com/en/#tag/Get-signed-document/operation/GetSignedDocumentPDF) |
| [Download XML](actions/download-xml.md) | `GET /api/v1/documents/:id/xml` | [docs](https://docs.mifiel.com/en/#tag/Get-signed-document/operation/GetSignedDocumentXML) |
| [Download ZIP File](actions/download-zip-file.md) | `GET /api/v1/documents/:id/zip` | [docs](https://docs.mifiel.com/en/#tag/Get-signed-document/operation/GetSignedDocumentZIP) |
| [Get Document](actions/get-document.md) | `GET /api/v1/documents/:id` | [docs](https://docs.mifiel.com/en/#tag/Document/operation/GetDocument) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v1/webhooks` | [docs](https://docs.mifiel.com/en/#tag/Webhooks/operation/GetWebhooks) |
| [Search Advanced Information](actions/search-advanced-information.md) | `POST /api/query` | [docs](https://docs.mifiel.com/en/#tag/Get-advanced-information/operation/QueryEndpoint) |
| [Update Stakeholder](actions/update-stakeholder.md) | `PUT /api/v1/documents/:documentId/stakeholders/:id` | [docs](https://docs.mifiel.com/en/#tag/Stakeholders/operation/UpdateStakeholder) |
