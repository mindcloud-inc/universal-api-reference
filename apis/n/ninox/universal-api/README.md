# <img src="https://images.mindcloud.co/apps/icons/ninox_1773758936539.png" alt="Ninox logo" width="28" height="28"> Ninox: Universal API

Manage Ninox workspaces, databases, tables, records, and files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ninox/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ninox.com
- **Vendor API docs:** https://forum.ninox.com/t/83yzlg7/introduction-to-ninox-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download File](actions/download-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/download-file?connectionId=$CONNECTION_ID&teamId=team_id&dbId=database_id&tableId=A&recordId=1&file=invoice.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Schema](actions/get-database-schema.md) | GET | Retrieves a database schema from Ninox. |
| [List Databases](actions/list-databases.md) | GET | Retrieves multiple databases from Ninox. |

### Database Change

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Changes](actions/get-database-changes.md) | GET | Retrieves database changes from Ninox by sequence number. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from a Ninox record. |
| [Download File](actions/download-file.md) | GET | Retrieves a file from a Ninox record. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to a Ninox record. |

### File Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves metadata for a file in Ninox. |
| [List File Metadata](actions/list-file-metadata.md) | GET | Retrieves metadata for files in a Ninox record. |

### File Thumbnail

| Action | Method | Description |
| --- | --- | --- |
| [Get File Thumbnail](actions/get-file-thumbnail.md) | GET | Retrieves a file thumbnail from a Ninox record. |

### Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Execute Read-Only Query Via GET](actions/execute-read-only-query-via-get.md) | GET | Executes a read-only database query in Ninox. |
| [Execute Read-Only Query Via POST](actions/execute-read-only-query-via-post.md) | GET | Executes a read-only database query in Ninox. |
| [Execute Writable Query](actions/execute-writable-query.md) | PUT | Executes a writable database query in Ninox. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Records](actions/create-or-update-records.md) | POST | Creates or updates multiple records in a Ninox table. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from a Ninox table. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes multiple records from a Ninox table. |
| [Find Record By POST](actions/find-record-by-post.md) | GET | Finds a record in Ninox by filters. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a Ninox table. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a Ninox table. |
| [Update Record](actions/update-record.md) | PUT | Updates a record in a Ninox table. |

### Record Change

| Action | Method | Description |
| --- | --- | --- |
| [Get Record Changes](actions/get-record-changes.md) | GET | Retrieves record changes from Ninox by sequence number. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Schema](actions/get-table-schema.md) | GET | Retrieves a table schema from Ninox. |
| [List Tables](actions/list-tables.md) | GET | Retrieves table schemas from Ninox. |

### Table Change

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Changes](actions/get-table-changes.md) | GET | Retrieves table changes from Ninox by sequence number. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Ninox. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves multiple workspaces from Ninox. |

