# List Projects with Hubflo

Retrieves all project records from Hubflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [List Projects](https://hubflo.readme.io/reference/get_api-v2-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `owner_id` | query | `string` | no |
| `owner_email` | query | `string` | no |
| `contact_id` | query | `string` | no |
| `contact_email` | query | `string` | no |
| `contact_phone` | query | `string` | no |
| `workspace_id` | query | `string` | no |
| `name` | query | `string` | no |
