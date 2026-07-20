# Dromo: Native API Reference

A consolidated summary of Dromo's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developer.dromo.io/api-reference
- **OpenAPI specification:** https://developer.dromo.io/api-reference/openapi.json
- **API base URL:** `https://app.dromo.io/api/v1`

## Authentication

### API Key

Use your Dromo backend license key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Dromo-License-Key: <apiKey>
```

[Official authentication documentation](https://developer.dromo.io/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Headless Import](actions/create-headless-import.md) | `POST /headless/imports/` | [docs](https://developer.dromo.io/api-reference/headless/create-a-new-headless-import) |
| [Create Import Schema](actions/create-import-schema.md) | `POST /schemas/` | [docs](https://developer.dromo.io/api-reference/import-schemas/create-a-new-import-schema) |
| [Create SFTP Connector](actions/create-sftp-connector.md) | `POST /headless/sftp/connectors/` | [docs](https://developer.dromo.io/api-reference/sftp-connectors/create-sftp-connector) |
| [Create SFTP Credentials](actions/create-sftp-credentials.md) | `POST /headless/sftp/credentials/` | [docs](https://developer.dromo.io/api-reference/sftp-credentials/create-sftp-credentials) |
| [Delete Headless Import](actions/delete-headless-import.md) | `DELETE /headless/imports/:id/` | [docs](https://developer.dromo.io/api-reference/headless/delete-headless-import) |
| [Delete Import Schema](actions/delete-import-schema.md) | `DELETE /schemas/:id/` | [docs](https://developer.dromo.io/api-reference/import-schemas/delete-an-import-schema) |
| [Delete SFTP Connector](actions/delete-sftp-connector.md) | `DELETE /headless/sftp/connectors/:id/` | [docs](https://developer.dromo.io/api-reference/sftp-connectors/delete-sftp-connector) |
| [Delete SFTP Credentials](actions/delete-sftp-credentials.md) | `DELETE /headless/sftp/credentials/:id/` | [docs](https://developer.dromo.io/api-reference/sftp-credentials/delete-sftp-credentials) |
| [Delete Upload Permanently](actions/delete-upload-permanently.md) | `POST /upload/:id/delete/` | [docs](https://developer.dromo.io/api-reference/uploads/delete-an-upload-permanently) |
| [Get Import Schema](actions/get-import-schema.md) | `GET /schemas/:id/` | [docs](https://developer.dromo.io/api-reference/import-schemas/get-an-import-schema) |
| [Get Presigned Download URL for Headless Import Data](actions/get-presigned-download-url-for-headless-import-data.md) | `GET /headless/imports/:id/url/` | [docs](https://developer.dromo.io/api-reference/headless/get-presigned-download-url-for-headless-import-data) |
| [Get Presigned Download URL for Upload Data](actions/get-presigned-download-url-for-upload-data.md) | `GET /upload/:id/url/` | [docs](https://developer.dromo.io/api-reference/uploads/get-presigned-download-url-for-upload-data) |
| [Get Upload Metadata](actions/get-upload-metadata.md) | `GET /upload/:id/metadata/` | [docs](https://developer.dromo.io/api-reference/uploads/get-upload-metadata) |
| [List Headless Imports](actions/list-headless-imports.md) | `GET /headless/imports/` | [docs](https://developer.dromo.io/api-reference/headless/list-headless-imports) |
| [List Import Schemas](actions/list-import-schemas.md) | `GET /schemas/` | [docs](https://developer.dromo.io/api-reference/import-schemas/get-all-import-schemas) |
| [List SFTP Connectors](actions/list-sftp-connectors.md) | `GET /headless/sftp/connectors/` | [docs](https://developer.dromo.io/api-reference/sftp-connectors/list-sftp-connectors) |
| [List SFTP Credentials](actions/list-sftp-credentials.md) | `GET /headless/sftp/credentials/` | [docs](https://developer.dromo.io/api-reference/sftp-credentials/list-sftp-credentials) |
| [List Uploads](actions/list-uploads.md) | `GET /uploads/` | [docs](https://developer.dromo.io/api-reference/uploads/get-all-uploads) |
| [Retrieve Headless Import](actions/retrieve-headless-import.md) | `GET /headless/imports/:id/` | [docs](https://developer.dromo.io/api-reference/headless/retrieve-headless-import) |
| [Retrieve SFTP Connector](actions/retrieve-sftp-connector.md) | `GET /headless/sftp/connectors/:id/` | [docs](https://developer.dromo.io/api-reference/sftp-connectors/retrieve-sftp-connector) |
| [Retrieve SFTP Credentials](actions/retrieve-sftp-credentials.md) | `GET /headless/sftp/credentials/:id/` | [docs](https://developer.dromo.io/api-reference/sftp-credentials/retrieve-sftp-credentials) |
| [Test SFTP Connection](actions/test-sftp-connection.md) | `POST /headless/sftp/credentials/:id/test_connection/` | [docs](https://developer.dromo.io/api-reference/sftp-credentials/test-sftp-connection) |
| [Update Import Schema](actions/update-import-schema.md) | `PUT /schemas/:id/` | [docs](https://developer.dromo.io/api-reference/import-schemas/update-an-import-schema) |
| [Update SFTP Connector](actions/update-sftp-connector.md) | `PUT /headless/sftp/connectors/:id/` | [docs](https://developer.dromo.io/api-reference/sftp-connectors/update-sftp-connector) |
| [Update SFTP Credentials](actions/update-sftp-credentials.md) | `PUT /headless/sftp/credentials/:id/` | [docs](https://developer.dromo.io/api-reference/sftp-credentials/update-sftp-credentials) |
