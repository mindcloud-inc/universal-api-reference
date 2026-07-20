# <img src="https://images.mindcloud.co/apps/icons/stackby_1776107751929.png" alt="Stackby logo" width="28" height="28"> Stackby: Universal API

Use Stackby's public API to manage workspaces, stacks, tables, columns, views, files, and rows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stackby/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stackby.com/
- **Vendor API docs:** https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Stacks](actions/list-stacks.md) | GET | Retrieves stacks from a Stackby workspace. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from a Stackby stack. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [List Columns](actions/list-columns.md) | GET | Retrieves columns from a Stackby table. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Row](actions/create-row.md) | POST | Creates a new row in a Stackby table. |
| [Create Rows Batch](actions/create-rows-batch.md) | POST | Creates new rows in a Stackby table. |
| [Delete Row](actions/delete-row.md) | DELETE | Deletes an existing row from a Stackby table. |
| [Delete Rows Batch](actions/delete-rows-batch.md) | DELETE | Deletes existing rows from a Stackby table. |
| [Filter Rows](actions/filter-rows.md) | GET | Finds rows in a Stackby table by filters. |
| [Get Rows By ID](actions/get-rows-by-id.md) | GET | Retrieves Stackby rows by ID. |
| [List Rows](actions/list-rows.md) | GET | Retrieves rows from a Stackby table. |
| [List Rows Latest](actions/list-rows-latest.md) | GET | Retrieves recently changed rows from a Stackby table. |
| [Paginate Rows](actions/paginate-rows.md) | GET | Retrieves paginated rows from a Stackby table. |
| [Sort Rows](actions/sort-rows.md) | GET | Retrieves sorted rows from a Stackby table. |
| [Update Row](actions/update-row.md) | PUT | Updates an existing row in a Stackby table. |
| [Update Rows Batch](actions/update-rows-batch.md) | PUT | Updates existing rows in a Stackby table. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Retrieves views from a Stackby table. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Stackby. |

