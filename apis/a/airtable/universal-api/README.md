# <img src="https://images.mindcloud.co/apps/icons/airtable_1773336776952.png" alt="Airtable logo" width="28" height="28"> Airtable: Universal API

Build apps, organize data, automate workflows, and collaborate across teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airtable/latest
- **Category:** Content & Files / Storage
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://airtable.com/developers/web/api/
- **Vendor API docs:** https://airtable.com/developers/web/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bases](actions/list-bases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-bases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Base

| Action | Method | Description |
| --- | --- | --- |
| [List Bases](actions/list-bases.md) | GET | Retrieves accessible bases from the Airtable account. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a specific Airtable table. |
| [Get Record](actions/get-record.md) | GET | Retrieves a specific record from an Airtable table. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a specific Airtable table. |
| [List Records - Compact](actions/list-records-compact.md) | GET | Retrieves selected fields from records in a specific Airtable table. |
| [Update Multiple Records](actions/update-multiple-records.md) | PUT | Updates multiple records in a specific Airtable table, or upserts them when enabled. |
| [Update Record](actions/update-record.md) | PUT | Updates a record in a specific Airtable table. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a new table in a specific Airtable base. |

