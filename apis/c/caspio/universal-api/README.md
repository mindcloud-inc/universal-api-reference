# <img src="https://images.mindcloud.co/apps/icons/images-1_1773680096632.jpeg" alt="Caspio logo" width="28" height="28"> Caspio: Universal API

Tenant-scoped Caspio REST API wrapper for tables, views, files, and record operations on d2hbw900.caspio.com.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/caspio/latest
- **Category:** IT Operations / Database
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.caspio.com/
- **Vendor API docs:** https://d2hbw900.caspio.com/integrations/rest/swagger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List File Folders](actions/list-file-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-file-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves detailed file metadata from Caspio. |
| [List Files](actions/list-files.md) | GET | Retrieves all available files from Caspio. |

### File Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get File Folder Metadata](actions/get-file-folder-metadata.md) | GET | Retrieves file folder metadata from Caspio. |
| [List File Folders](actions/list-file-folders.md) | GET | Retrieves all file folders from Caspio. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Table](actions/get-table.md) | GET | Retrieves a single table from Caspio. |
| [List Tables](actions/list-tables.md) | GET | Retrieves all available tables from Caspio. |

### Table Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Table Attachment](actions/delete-table-attachment.md) | DELETE | Deletes a table attachment from Caspio. |
| [Download Table Attachment](actions/download-table-attachment.md) | GET | Downloads a table attachment from Caspio. |
| [Get Table Attachment Metadata](actions/get-table-attachment-metadata.md) | GET | Retrieves table attachment metadata from Caspio. |
| [Rename Table Attachment](actions/rename-table-attachment.md) | PUT | Updates table attachment metadata in Caspio. |
| [Upload Table Attachment](actions/upload-table-attachment.md) | PUT | Uploads a table attachment to Caspio. |

### Table Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Field](actions/get-table-field.md) | GET | Retrieves a table field from Caspio. |
| [List Table Fields](actions/list-table-fields.md) | GET | Retrieves all table fields from Caspio. |

### Table Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Table Record](actions/create-table-record.md) | POST | Creates a new table record in Caspio. |
| [Delete Table Records](actions/delete-table-records.md) | DELETE | Deletes existing table records from Caspio. |
| [List Table Records](actions/list-table-records.md) | GET | Retrieves all table records from Caspio. |
| [Update Table Records](actions/update-table-records.md) | PUT | Updates existing table records in Caspio. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [Get View](actions/get-view.md) | GET | Retrieves a single view from Caspio. |
| [List Views](actions/list-views.md) | GET | Retrieves all available views from Caspio. |

### View Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete View Attachment](actions/delete-view-attachment.md) | DELETE | Deletes a view attachment from Caspio. |
| [Download View Attachment](actions/download-view-attachment.md) | GET | Downloads a view attachment from Caspio. |
| [Get View Attachment Metadata](actions/get-view-attachment-metadata.md) | GET | Retrieves view attachment metadata from Caspio. |
| [Rename View Attachment](actions/rename-view-attachment.md) | PUT | Updates view attachment metadata in Caspio. |
| [Upload View Attachment](actions/upload-view-attachment.md) | PUT | Uploads a view attachment to Caspio. |

### View Field

| Action | Method | Description |
| --- | --- | --- |
| [Get View Field](actions/get-view-field.md) | GET | Retrieves a view field from Caspio. |
| [List View Fields](actions/list-view-fields.md) | GET | Retrieves all view fields from Caspio. |

### View Record

| Action | Method | Description |
| --- | --- | --- |
| [Create View Record](actions/create-view-record.md) | POST | Creates a new view record in Caspio. |
| [Delete View Records](actions/delete-view-records.md) | DELETE | Deletes existing view records from Caspio. |
| [List View Records](actions/list-view-records.md) | GET | Retrieves all view records from Caspio. |
| [Update View Records](actions/update-view-records.md) | PUT | Updates existing view records in Caspio. |

