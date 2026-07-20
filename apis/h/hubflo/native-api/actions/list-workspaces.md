# List Workspaces with Hubflo

Retrieves all workspace records from Hubflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [List Workspaces](https://hubflo.readme.io/reference/get_api-v2-workspaces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `project_id` | query | `string` | no |
| `workspace_id` | query | `string` | no |
| `title` | query | `string` | no |
