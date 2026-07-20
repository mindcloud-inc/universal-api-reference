# List Projects with Leadspicker

Retrieves projects from Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/projects`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [List Projects](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_get_project_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Search projects by name, labels, or contacts. |
| `limit` | query | `number` | no | Maximum number of projects to return. |
| `order_by_field` | query | `list<string>` | no | Project ordering field: created, last_active, name, or pk. Accepted values: `0`, `1`, `2`, `3`. |
| `order_direction` | query | `list<string>` | no | Project ordering direction: asc or desc. Accepted values: `0`, `1`. |
