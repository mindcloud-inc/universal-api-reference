# <img src="https://images.mindcloud.co/apps/icons/gridly_1776796749921.png" alt="Gridly logo" width="28" height="28"> Gridly: Universal API

Gridly is a localization and structured content platform for managing projects, databases, grids, views, records, glossaries, translation memories, automations, and delivery workflows through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gridly/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gridly.com
- **Vendor API docs:** https://www.gridly.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Branches

| Action | Method | Description |
| --- | --- | --- |
| [Get Branch](actions/get-branch.md) | GET | Retrieves a branch from Gridly by branch ID. |
| [List Branches](actions/list-branches.md) | GET | Finds branches in Gridly by grid ID. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Create Column](actions/create-column.md) | POST | Creates a new column in a Gridly view. |
| [Delete Column](actions/delete-column.md) | DELETE | Deletes an existing column from a Gridly view. |
| [Get Column](actions/get-column.md) | GET | Retrieves a column from Gridly by column ID. |
| [Update Column](actions/update-column.md) | PUT | Updates an existing column in a Gridly view. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Get Database](actions/get-database.md) | GET | Retrieves a database from Gridly by database ID. |
| [List Databases](actions/list-databases.md) | GET | Finds databases in your Gridly workspace. |

### Dependencies

| Action | Method | Description |
| --- | --- | --- |
| [Create Dependency](actions/create-dependency.md) | POST | Creates a new dependency in a Gridly view. |
| [Delete Dependency](actions/delete-dependency.md) | DELETE | Deletes an existing dependency from a Gridly view. |
| [Get Dependency](actions/get-dependency.md) | GET | Retrieves a dependency from Gridly by dependency ID. |
| [List Dependencies](actions/list-dependencies.md) | GET | Finds dependencies in a specific Gridly view. |
| [Update Dependency](actions/update-dependency.md) | PUT | Updates an existing dependency in a Gridly view. |

### Grid

| Action | Method | Description |
| --- | --- | --- |
| [Create Grid](actions/create-grid.md) | POST | Creates a new grid in Gridly. |
| [Delete Grid](actions/delete-grid.md) | DELETE | Deletes an existing grid from Gridly. |
| [Get Grid](actions/get-grid.md) | GET | Retrieves a grid from Gridly by grid ID. |
| [List Grids](actions/list-grids.md) | GET | Finds grids in Gridly by database ID. |
| [Update Grid](actions/update-grid.md) | PUT | Updates an existing grid in Gridly. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Gridly by project ID. |
| [List Projects](actions/list-projects.md) | GET | Finds projects in your Gridly workspace. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [List Records](actions/list-records.md) | GET | Finds records in a specific Gridly view. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Create View](actions/create-view.md) | POST | Creates a new view in Gridly. |
| [Delete View](actions/delete-view.md) | DELETE | Deletes an existing view from Gridly. |
| [Get View](actions/get-view.md) | GET | Retrieves a view from Gridly by view ID. |
| [List Views](actions/list-views.md) | GET | Finds views in Gridly by grid or branch. |

