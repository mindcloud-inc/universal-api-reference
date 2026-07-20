# <img src="https://images.mindcloud.co/apps/icons/zoho-tables_1774034752271.png" alt="Zoho Tables logo" width="28" height="28"> Zoho Tables: Universal API

Manage Zoho Tables workspaces, bases, tables, fields, and records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoTables/latest
- **Category:** IT Operations / Database
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tables.zoho.com
- **Vendor API docs:** https://tables.zoho.com/help/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Portals](actions/list-portals.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Base](actions/create-base.md) | POST | Creates a new base in Zoho Tables. |
| [Delete Base](actions/delete-base.md) | DELETE | Deletes an existing base from Zoho Tables. |
| [Duplicate Base](actions/duplicate-base.md) | POST | Creates a duplicate base in Zoho Tables. |
| [List Base](actions/list-base.md) | GET | Retrieves all bases from Zoho Tables. |
| [Search Bases](actions/search-bases.md) | GET | Finds bases in Zoho Tables by search string. |
| [Update Base](actions/update-base.md) | PUT | Updates an existing base in Zoho Tables. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in Zoho Tables. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from Zoho Tables. |
| [List Fields](actions/list-fields.md) | GET | Retrieves all fields from Zoho Tables. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in Zoho Tables. |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [List Portals](actions/list-portals.md) | GET | Retrieves all portals from Zoho Tables. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in Zoho Tables. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from Zoho Tables. |
| [Fetch Records with Criteria](actions/fetch-records-with-criteria.md) | GET | Finds records in Zoho Tables by criteria or record IDs. |
| [List Records](actions/list-records.md) | GET | Retrieves table records from Zoho Tables. |
| [Update Records](actions/update-records.md) | PUT | Updates records in Zoho Tables by criteria or record IDs. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a new table in Zoho Tables. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes an existing table from Zoho Tables. |
| [Duplicate Table](actions/duplicate-table.md) | POST | Creates a duplicate table in Zoho Tables. |
| [List Tables](actions/list-tables.md) | GET | Retrieves all tables from Zoho Tables. |
| [Update Table](actions/update-table.md) | PUT | Updates an existing table in Zoho Tables. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Retrieves all views from Zoho Tables. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Zoho Tables. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves all workspaces from Zoho Tables. |

