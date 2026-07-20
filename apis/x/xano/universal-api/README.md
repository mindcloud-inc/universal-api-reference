# <img src="https://images.mindcloud.co/apps/icons/xano-icon-square_1775763658508.png" alt="Xano logo" width="28" height="28"> Xano: Universal API

Manage Xano metadata resources including workspaces, API groups, APIs, branches, tables, content, files, functions, tasks, tenants, and related administrative surfaces through the Xano Metadata API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xano/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xano.com
- **Vendor API docs:** https://docs.xano.com/xano-features/metadata-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Branches

| Action | Method | Description |
| --- | --- | --- |
| [Create Branch](actions/create-branch.md) | POST | Creates a new branch in a Xano workspace. |
| [Delete Branch](actions/delete-branch.md) | DELETE | Deletes an existing branch from Xano. |
| [Get Branch](actions/get-branch.md) | GET | Retrieves a branch from Xano by label. |
| [List Branches](actions/list-branches.md) | GET | Finds branches in a Xano workspace. |
| [Set Live Branch](actions/set-live-branch.md) | PUT | Sets a branch as live in Xano. |
| [Update Branch](actions/update-branch.md) | PUT | Updates an existing branch in Xano. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a new table in a Xano workspace. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes an existing table from Xano. |
| [Get Table](actions/get-table.md) | GET | Retrieves a table from Xano by ID. |
| [List Tables](actions/list-tables.md) | GET | Finds tables in a Xano workspace. |
| [Update Table](actions/update-table.md) | PUT | Updates an existing table in Xano. |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create API](actions/create-api.md) | POST | Creates a new API endpoint in Xano. |
| [Delete API](actions/delete-api.md) | DELETE | Deletes an existing API endpoint from Xano. |
| [Get API](actions/get-api.md) | GET | Retrieves an API endpoint from Xano by ID. |
| [Get API Group OpenAPI](actions/get-api-group-openapi.md) | GET | Retrieves an OpenAPI specification for a Xano API group. |
| [Get API OpenAPI](actions/get-api-openapi.md) | GET | Retrieves an OpenAPI specification for a Xano API endpoint. |
| [List APIs](actions/list-apis.md) | GET | Finds API endpoints in a Xano API group. |
| [Update API](actions/update-api.md) | PUT | Updates an existing API endpoint in Xano. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create API Group](actions/create-api-group.md) | POST | Creates a new API group in a Xano workspace. |
| [Delete API Group](actions/delete-api-group.md) | DELETE | Deletes an existing API group from Xano. |
| [Get API Group](actions/get-api-group.md) | GET | Retrieves an API group from Xano by ID. |
| [List API Groups](actions/list-api-groups.md) | GET | Finds API groups in a Xano workspace. |
| [Update API Group](actions/update-api-group.md) | PUT | Updates an existing API group in Xano. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Table Record](actions/create-table-record.md) | POST | Creates a new record in a Xano table. |
| [Delete Table Record](actions/delete-table-record.md) | DELETE | Deletes an existing record from a Xano table. |
| [Get Table Record](actions/get-table-record.md) | GET | Retrieves a record from a Xano table by ID. |
| [List Table Records](actions/list-table-records.md) | GET | Finds records in a Xano table. |
| [Search Table Records](actions/search-table-records.md) | GET | Finds records in a Xano table by search filters. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Xano. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Xano. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from Xano. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Xano by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Finds workspaces in Xano. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Xano. |

