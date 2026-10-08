# <img src="https://images.mindcloud.co/apps/icons/fleetworthy_1788529777637.png" alt="Fleetworthy logo" width="28" height="28"> Fleetworthy: Universal API

Manage driver compliance records, regulated documents, and related files in Fleetworthy.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fleetworthy/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fleetworthy.com
- **Vendor API docs:** https://developer.fleetworthy.com/api-details

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Asset File](actions/download-asset-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-asset-file?connectionId=$CONNECTION_ID&cpFileId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate User Token](actions/generate-user-token.md) | POST |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET |  |
| [Get Asset Client Metadata](actions/get-asset-client-metadata.md) | GET |  |
| [Get Asset Import Progress](actions/get-asset-import-progress.md) | GET |  |
| [Get Asset Import Schema](actions/get-asset-import-schema.md) | GET |  |
| [Get Asset Metadata](actions/get-asset-metadata.md) | GET |  |
| [Get Asset Procurement Information](actions/get-asset-procurement-information.md) | GET |  |
| [Get Asset Schema](actions/get-asset-schema.md) | GET |  |
| [Get Asset Specification](actions/get-asset-specification.md) | GET |  |
| [List Asset Specification History](actions/list-asset-specification-history.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Regulated Document](actions/create-person-regulated-document.md) | POST |  |
| [Get Asset Document](actions/get-asset-document.md) | GET |  |
| [Get Asset Document Schema](actions/get-asset-document-schema.md) | GET |  |
| [Get People Client Metadata](actions/get-people-client-metadata.md) | GET |  |
| [Get Person File Info](actions/get-person-file-info.md) | GET |  |
| [Get Person Metadata](actions/get-person-metadata.md) | GET |  |
| [List Person Company Documents](actions/list-person-company-documents.md) | GET |  |
| [List Person Regulated Documents](actions/list-person-regulated-documents.md) | GET |  |
| [Search Regulated Documents](actions/search-regulated-documents.md) | GET |  |
| [Upload Person File](actions/upload-person-file.md) | POST |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get People Import Progress](actions/get-people-import-progress.md) | GET |  |
| [Get Person](actions/get-person.md) | GET |  |
| [Search People](actions/search-people.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Asset File](actions/download-asset-file.md) | GET |  |
| [Download Latest Report](actions/download-latest-report.md) | GET |  |
| [Download Person File](actions/download-person-file.md) | GET |  |
| [Download Report File](actions/download-report-file.md) | GET |  |
| [Get Asset File Info](actions/get-asset-file-info.md) | GET |  |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Get API Health](actions/get-api-health.md) | GET |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Asset Document Notes](actions/list-asset-document-notes.md) | GET |  |
| [List Asset Notes](actions/list-asset-notes.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Report Runs](actions/list-report-runs.md) | GET |  |
| [List Reporting Configurations](actions/list-reporting-configurations.md) | GET |  |

