# <img src="https://images.mindcloud.co/apps/icons/data-blaze-icon-filled-256_1774544959674.png" alt="Data Blaze logo" width="28" height="28"> Data Blaze: Universal API

Connect to Data Blaze and work with rows in the Mindcloud table. Stage 1 is scaffolded against the official REST API and a fixed safe read action for the Mindcloud table.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataBlaze/latest
- **Category:** IT Operations / Database
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://blaze.today/datablaze/
- **Vendor API docs:** https://blaze.today/datablaze/docs/apis/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Table Rows](actions/list-table-rows.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-rows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Table Fields](actions/list-table-fields.md) | GET | Retrieves table fields from Data Blaze. |

### Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Run SQL Query](actions/run-sql-query.md) | GET | Runs a SQL query in Data Blaze. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Create Table Row](actions/create-table-row.md) | POST | Creates a new table row in Data Blaze. |
| [Delete Table Row](actions/delete-table-row.md) | DELETE | Deletes an existing table row from Data Blaze. |
| [Get Table Row](actions/get-table-row.md) | GET | Retrieves a table row from Data Blaze. |
| [List Table Rows](actions/list-table-rows.md) | GET | Retrieves table rows from Data Blaze. |
| [Move Table Row](actions/move-table-row.md) | PUT | Moves a table row in Data Blaze. |
| [Update Table Row](actions/update-table-row.md) | PUT | Updates an existing table row in Data Blaze. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [List Accessible Tables](actions/list-accessible-tables.md) | GET | Retrieves accessible tables from Data Blaze. |

