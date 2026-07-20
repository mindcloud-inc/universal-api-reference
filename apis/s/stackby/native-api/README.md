# Stackby: Native API Reference

A consolidated summary of Stackby's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api
- **API base URL:** `https://stackby.com/api`

## Authentication

### API Key

Use a Stackby API key in the provider-required api-key header.

### Credentials

- **API Key:** `apiKey` · required · Your Stackby API key from Account settings. Stored once and injected as the shared api-key header.

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Row](actions/create-row.md) | `POST /betav1/rowcreate/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Create Rows Batch](actions/create-rows-batch.md) | `POST /betav1/rowcreate/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Delete Row](actions/delete-row.md) | `DELETE /betav1/rowdelete/{{stackId}}/{{tableName}}?rowIds[]={{rowId}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Delete Rows Batch](actions/delete-rows-batch.md) | `DELETE /betav1/rowdelete/{{stackId}}/{{tableName}}?{{rowIdsQuery}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Filter Rows](actions/filter-rows.md) | `GET /betav1/rowlist/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Get Rows By ID](actions/get-rows-by-id.md) | `GET /betav1/rowlist/{{stackId}}/{{tableName}}?{{rowIdsQuery}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [List Columns](actions/list-columns.md) | `GET /v0/columnlist/{{stackId}}/{{tableId}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api) |
| [List Rows](actions/list-rows.md) | `GET /betav1/rowlist/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [List Rows Latest](actions/list-rows-latest.md) | `GET /v0/rowlist/{{stackId}}/{{tableName}}?latest=true` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api) |
| [List Stacks](actions/list-stacks.md) | `GET /v0/stacklist/{{workspaceId}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api) |
| [List Tables](actions/list-tables.md) | `GET /v0/tablelist/{{stackId}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api) |
| [List Views](actions/list-views.md) | `GET /v0/viewlist/{{stackId}}/{{tableId}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v0/workspacelist` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api) |
| [Paginate Rows](actions/paginate-rows.md) | `GET /betav1/rowlist/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Sort Rows](actions/sort-rows.md) | `GET /betav1/rowlist/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Update Row](actions/update-row.md) | `PATCH /betav1/rowupdate/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
| [Update Rows Batch](actions/update-rows-batch.md) | `PATCH /betav1/rowupdate/{{stackId}}/{{tableName}}` | [docs](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api) |
