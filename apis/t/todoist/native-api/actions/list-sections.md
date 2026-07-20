# List Sections with Todoist

Retrieves sections from Todoist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/sections`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [List Sections](https://developer.todoist.com/api/v1/#tag/Sections/operation/get_sections_api_v1_sections_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | Optional project ID to return sections for a specific project. |
| `cursor` | query | `string` | no | Cursor for the next page of results. |
| `limit` | query | `number` | no | Maximum number of results to return. |
| `public_key` | query | `string` | no | Public key used for shared-resource access where applicable. |
