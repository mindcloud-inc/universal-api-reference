# <img src="https://images.mindcloud.co/apps/icons/dromo_1775064126866.png" alt="Dromo logo" width="28" height="28"> Dromo: Universal API

Manage Dromo imports, uploads, schemas, and SFTP automation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dromo/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dromo.io
- **Vendor API docs:** https://developer.dromo.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Import Schemas](actions/list-import-schemas.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/list-import-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Headless Import

| Action | Method | Description |
| --- | --- | --- |
| [Create Headless Import](actions/create-headless-import.md) | POST | Creates a new headless import in Dromo. |
| [Delete Headless Import](actions/delete-headless-import.md) | DELETE | Deletes a headless import from Dromo. |
| [Get Presigned Download URL for Headless Import Data](actions/get-presigned-download-url-for-headless-import-data.md) | GET | Retrieves a presigned download URL for headless import data from Dromo. |
| [List Headless Imports](actions/list-headless-imports.md) | GET | Retrieves all headless imports from Dromo. |
| [Retrieve Headless Import](actions/retrieve-headless-import.md) | GET | Retrieves a headless import from Dromo. |

### Import Schema

| Action | Method | Description |
| --- | --- | --- |
| [Create Import Schema](actions/create-import-schema.md) | POST | Creates a new import schema in Dromo. |
| [Delete Import Schema](actions/delete-import-schema.md) | DELETE | Deletes an existing import schema from Dromo. |
| [Get Import Schema](actions/get-import-schema.md) | GET | Retrieves an import schema from Dromo. |
| [List Import Schemas](actions/list-import-schemas.md) | GET | Retrieves all import schemas from Dromo. |
| [Update Import Schema](actions/update-import-schema.md) | PUT | Updates an existing import schema in Dromo. |

### Sftp Connector

| Action | Method | Description |
| --- | --- | --- |
| [Create SFTP Connector](actions/create-sftp-connector.md) | POST | Creates a new SFTP connector in Dromo. |
| [Delete SFTP Connector](actions/delete-sftp-connector.md) | DELETE | Deletes an existing SFTP connector from Dromo. |
| [List SFTP Connectors](actions/list-sftp-connectors.md) | GET | Retrieves all SFTP connectors from Dromo. |
| [Retrieve SFTP Connector](actions/retrieve-sftp-connector.md) | GET | Retrieves an SFTP connector from Dromo. |
| [Update SFTP Connector](actions/update-sftp-connector.md) | PUT | Updates an existing SFTP connector in Dromo. |

### Sftp Credential

| Action | Method | Description |
| --- | --- | --- |
| [Create SFTP Credentials](actions/create-sftp-credentials.md) | POST | Creates new SFTP credentials in Dromo. |
| [Delete SFTP Credentials](actions/delete-sftp-credentials.md) | DELETE | Deletes existing SFTP credentials from Dromo. |
| [List SFTP Credentials](actions/list-sftp-credentials.md) | GET | Retrieves all SFTP credentials from Dromo. |
| [Retrieve SFTP Credentials](actions/retrieve-sftp-credentials.md) | GET | Retrieves SFTP credential details from Dromo. |
| [Test SFTP Connection](actions/test-sftp-connection.md) | GET | Tests an SFTP credential connection in Dromo. |
| [Update SFTP Credentials](actions/update-sftp-credentials.md) | PUT | Updates existing SFTP credentials in Dromo. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Delete Upload Permanently](actions/delete-upload-permanently.md) | DELETE | Deletes an upload permanently from Dromo. |
| [Get Presigned Download URL for Upload Data](actions/get-presigned-download-url-for-upload-data.md) | GET | Retrieves a presigned download URL for upload data from Dromo. |
| [Get Upload Metadata](actions/get-upload-metadata.md) | GET | Retrieves metadata for an upload from Dromo. |
| [List Uploads](actions/list-uploads.md) | GET | Retrieves all upload records from Dromo. |

