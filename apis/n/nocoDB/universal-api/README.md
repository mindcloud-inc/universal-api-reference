# <img src="https://images.mindcloud.co/apps/icons/nocodb_1774297909065.png" alt="NocoDB logo" width="28" height="28"> NocoDB: Universal API

NocoDB: Manage bases, tables, fields, and records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nocoDB/latest
- **Category:** IT Operations / Database
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nocodb.com
- **Vendor API docs:** https://nocodb.com/docs/product-docs/developer-resources/rest-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Attachment to Cell](actions/upload-attachment-to-cell.md) | POST | Uploads an attachment to a NocoDB cell. |

### Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Base](actions/create-base.md) | POST | Creates a new base in NocoDB. |
| [Delete Base](actions/delete-base.md) | DELETE | Deletes an existing base from NocoDB. |
| [Get Base](actions/get-base.md) | GET | Retrieves details for a base from NocoDB. |
| [List Bases](actions/list-bases.md) | GET | Retrieves bases in a NocoDB workspace. |
| [Update Base](actions/update-base.md) | PUT | Updates details for a base in NocoDB. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in a NocoDB table. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from NocoDB. |
| [Get Field](actions/get-field.md) | GET | Retrieves details for a field from NocoDB. |
| [Update Field](actions/update-field.md) | PUT | Updates details for a field in NocoDB. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Count Table Records](actions/count-table-records.md) | GET | Counts records in a NocoDB table. |
| [Create Table Records](actions/create-table-records.md) | POST | Creates new records in a NocoDB table. |
| [Delete Table Records](actions/delete-table-records.md) | DELETE | Deletes records from a NocoDB table. |
| [Get Record](actions/get-record.md) | GET | Retrieves a single record from a NocoDB table. |
| [Link Records](actions/link-records.md) | POST | Links records through a NocoDB link field. |
| [List Linked Records](actions/list-linked-records.md) | GET | Retrieves linked records from a NocoDB link field. |
| [List Table Records](actions/list-table-records.md) | GET | Retrieves records from a NocoDB table. |
| [Unlink Records](actions/unlink-records.md) | DELETE | Unlinks records from a NocoDB link field. |
| [Update Table Records](actions/update-table-records.md) | PUT | Updates records in a NocoDB table. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a new table in NocoDB. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes an existing table from NocoDB. |
| [Get Table](actions/get-table.md) | GET | Retrieves table schema details from NocoDB. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables in a NocoDB base. |
| [Rename Table](actions/rename-table.md) | PUT |  |
| [Update Table Description](actions/update-table-description.md) | PUT |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves accessible workspaces from your NocoDB account. |

