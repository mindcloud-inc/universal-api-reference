# List Projects with Todoist

Retrieves projects from Todoist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [List Projects](https://developer.todoist.com/api/v1/#tag/Projects/operation/get_projects_api_v1_projects_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of projects to return. |
| `cursor` | query | `string` | no | Pagination cursor returned from previous list response. |
