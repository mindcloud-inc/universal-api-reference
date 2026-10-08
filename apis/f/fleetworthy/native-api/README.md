# Fleetworthy: Native API Reference

A consolidated summary of Fleetworthy's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developer.fleetworthy.com/api-details
- **API base URL:** `https://apis.fleetworthy.com/compliance-api/v1`

## Authentication

### API Key and Password

Connect with a Fleetworthy API key and password. The connection automatically generates the user token required by Compliance API actions.

### Credentials

- **API Key:** `apiKey` · required · The API key issued for the Fleetworthy Compliance API.
- **Password:** `password` · required · The password for the Fleetworthy user associated with the API key.

Send these headers with each API request:

```http
X-User-Token: <custom.response>
Authorization: <apiKey>
```

[Official authentication documentation](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-token)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `itemsPerPage` in the request body to set the page size. Use `page` in the request body to choose the page; numbering starts at 0.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Person Regulated Document](actions/create-person-regulated-document.md) | `POST /people-documents/regulated` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-documents-regulated) |
| [Download Asset File](actions/download-asset-file.md) | `GET /assets/files/:cpFileId/download` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-files-cpfileid-download) |
| [Download Latest Report](actions/download-latest-report.md) | `GET /reporting/report-download-latest/:reportDisplayId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-reporting-report-download-latest-reportdisplayid) |
| [Download Person File](actions/download-person-file.md) | `GET /people/files/:cpFileId/download` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-files-cpfileid-download) |
| [Download Report File](actions/download-report-file.md) | `GET /reporting/report-download/:cpFileId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-reporting-report-download-cpfileid) |
| [Generate User Token](actions/generate-user-token.md) | `GET /token` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-token) |
| [Get API Health](actions/get-api-health.md) | `GET /health` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-health) |
| [Get Asset](actions/get-asset.md) | `GET /assets/:assetId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-assetid) |
| [Get Asset Client Metadata](actions/get-asset-client-metadata.md) | `GET /assets/client-metadata/:clientIdOrDisplayId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-client-metadata-clientidordisplayid) |
| [Get Asset Document](actions/get-asset-document.md) | `GET /assets/documents/:documentId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-documents-documentid) |
| [Get Asset Document Schema](actions/get-asset-document-schema.md) | `GET /assets/documents/schema` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-documents-schema) |
| [Get Asset File Info](actions/get-asset-file-info.md) | `GET /assets/file-info` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-file-info) |
| [Get Asset Import Progress](actions/get-asset-import-progress.md) | `GET /assets/bulk/import/progress/:importProcessId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-bulk-import-progress-importprocessid) |
| [Get Asset Import Schema](actions/get-asset-import-schema.md) | `GET /assets/bulk/import/schema` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-bulk-import-schema) |
| [Get Asset Metadata](actions/get-asset-metadata.md) | `GET /assets/metadata` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-metadata) |
| [Get Asset Procurement Information](actions/get-asset-procurement-information.md) | `GET /assets/procurement/:assetId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-procurement-assetid) |
| [Get Asset Schema](actions/get-asset-schema.md) | `GET /assets/bulk/import/asset-schema` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-bulk-import-asset-schema) |
| [Get Asset Specification](actions/get-asset-specification.md) | `GET /asset-specifications/:assetSpecificationId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-asset-specifications-assetspecificationid) |
| [Get People Client Metadata](actions/get-people-client-metadata.md) | `GET /people/client-metadata/{clientIdOrDisplayId}` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-client-metadata-clientidordisplayid) |
| [Get People Import Progress](actions/get-people-import-progress.md) | `GET /people-bulk/import/progress/:importProcessId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-bulk-import-progress-importprocessid) |
| [Get Person](actions/get-person.md) | `GET /people/{personIdOrDisplayId}` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-personidordisplayid) |
| [Get Person File Info](actions/get-person-file-info.md) | `GET /people/file-info` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-file-info) |
| [Get Person Metadata](actions/get-person-metadata.md) | `GET /people/metadata` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-metadata) |
| [List Asset Document Notes](actions/list-asset-document-notes.md) | `GET /assets/documents/asset-document-notes/from-parent/:parentId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-documents-asset-document-notes-from-parent-parentid) |
| [List Asset Notes](actions/list-asset-notes.md) | `GET /assets/notes/by-asset-id/:assetId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-notes-by-asset-id-assetid) |
| [List Asset Specification History](actions/list-asset-specification-history.md) | `GET /asset-specifications/:assetSpecificationId/history` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-asset-specifications-assetspecificationid-history) |
| [List Person Company Documents](actions/list-person-company-documents.md) | `GET /people-documents/company/:personId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-documents-company-personid) |
| [List Person Regulated Documents](actions/list-person-regulated-documents.md) | `GET /people-documents/regulated/{personId}` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-documents-regulated-personid) |
| [List Report Runs](actions/list-report-runs.md) | `GET /reporting/report-runs/:reportDisplayId` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-reporting-report-runs-reportdisplayid) |
| [List Reporting Configurations](actions/list-reporting-configurations.md) | `GET /reporting/configs` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-reporting-configs) |
| [Search People](actions/search-people.md) | `POST /people-bulk/search` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-bulk-search) |
| [Search Regulated Documents](actions/search-regulated-documents.md) | `POST /people-bulk/regulated-documents/search` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-bulk-regulated-documents-search) |
| [Upload Person File](actions/upload-person-file.md) | `POST /people/files` | [docs](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-files) |
