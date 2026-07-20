# Zoho Sign: Native API Reference

A consolidated summary of Zoho Sign's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/sign/api/
- **OpenAPI specification:** https://api.swaggerhub.com/apis/zohosign/zohosign_api/1.0.0/swagger.json
- **API base URL:** `https://sign.zoho.com/api/v1`

## Authentication

### OAuth2

### Credentials

- **Zoho Domain:** `zohoDomain` · required · Zoho data center suffix such as com, eu, in, jp, com.au, zohocloud.ca, or sa.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoSign.documents.CREATE,ZohoSign.documents.READ,ZohoSign.documents.UPDATE,ZohoSign.templates.CREATE,ZohoSign.templates.READ,ZohoSign.templates.UPDATE,ZohoSign.account.CREATE,ZohoSign.account.READ,ZohoSign.account.UPDATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/sign/api/oauth.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Correct Document](actions/correct-document.md) | `POST /requests/:requestId/markforcorrection` | [docs](https://www.zoho.com/sign/api/document-managment/correct-document.html) |
| [Create Document](actions/create-document.md) | `POST /requests` | [docs](https://www.zoho.com/sign/api/document-managment/create-document.html) |
| [Create Document Type](actions/create-document-type.md) | `POST /requesttypes` | [docs](https://www.zoho.com/sign/api/document-managment/create-new-document-type.html) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://www.zoho.com/sign/api/document-managment/create-new-folder.html) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://www.zoho.com/sign/api/template-managment/create-template.html) |
| [Delete Document](actions/delete-document.md) | `PUT /requests/:requestId/delete` | [docs](https://www.zoho.com/sign/api/document-managment/delete-document.html) |
| [Delete Template](actions/delete-template.md) | `PUT /templates/:templateId/delete` | [docs](https://www.zoho.com/sign/api/template-managment/delete-template.html) |
| [Download Document PDF](actions/download-document-pdf.md) | `GET /requests/:requestId/pdf` | [docs](https://www.zoho.com/sign/api/document-managment/download-pdf.html) |
| [Download Particular PDF File](actions/download-particular-pdf-file.md) | `GET /requests/:requestId/documents/:documentId/pdf` | [docs](https://www.zoho.com/sign/api/document-managment/download-particular-pdf.html) |
| [Extend Document Expiry](actions/extend-document-expiry.md) | `PUT /requests/:requestId/extend` | [docs](https://www.zoho.com/sign/api/document-managment/extend-document.html) |
| [Get Document Details](actions/get-document-details.md) | `GET /requests/:requestId` | [docs](https://www.zoho.com/sign/api/document-managment/get-details-of-a-particular-document.html) |
| [Get Document Form Data](actions/get-document-form-data.md) | `GET /requests/:requestId/fielddata` | [docs](https://www.zoho.com/sign/api/document-managment/get-document-form-data.html) |
| [Get Template Details](actions/get-template-details.md) | `GET /templates/:templateId` | [docs](https://www.zoho.com/sign/api/template-managment/get-template-details.html) |
| [List Document Types](actions/list-document-types.md) | `GET /requesttypes` | [docs](https://www.zoho.com/sign/api/document-managment/get-document-type.html) |
| [List Documents](actions/list-documents.md) | `GET /requests` | [docs](https://www.zoho.com/sign/api/document-managment/get-document-list.html) |
| [List Field Types](actions/list-field-types.md) | `GET /fieldtypes` | [docs](https://www.zoho.com/sign/api/document-managment/retrieve-field-type.html) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://www.zoho.com/sign/api/document-managment/get-folder-list.html) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://www.zoho.com/sign/api/template-managment/get-template-list.html) |
| [Recall Document](actions/recall-document.md) | `POST /requests/:requestId/recall` | [docs](https://www.zoho.com/sign/api/document-managment/recall-document.html) |
| [Remind Recipient](actions/remind-recipient.md) | `POST /requests/:requestId/remind` | [docs](https://www.zoho.com/sign/api/document-managment/remind-recipient.html) |
| [Send Document Using Template](actions/send-document-using-template.md) | `POST /templates/:templateId/createdocument` | [docs](https://www.zoho.com/sign/api/template-managment/send-documents-using-template.html) |
| [Submit Document](actions/submit-document.md) | `POST /requests/:requestId/submit` | [docs](https://www.zoho.com/sign/api/document-managment/send-document-for-signature.html) |
| [Update Document](actions/update-document.md) | `PUT /requests/:requestId` | [docs](https://www.zoho.com/sign/api/document-managment/update-document.html) |
