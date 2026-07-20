# List Companies with Hubflo

Retrieves all company records from Hubflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [List Companies](https://hubflo.readme.io/reference/get_api-v2-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | query | `string` | no |
| `name` | query | `string` | no |
| `owner_id` | query | `string` | no |
| `page` | query | `number` | no |
| `parent_id` | query | `string` | no |
| `project_id` | query | `string` | no |
| `per_page` | query | `number` | no |
