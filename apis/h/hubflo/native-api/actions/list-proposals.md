# List Proposals with Hubflo

Retrieves all proposal records from Hubflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/proposals`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [List Proposals](https://hubflo.readme.io/reference/get_api-v2-proposals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `contact_id` | query | `string` | no |
| `project_id` | query | `string` | no |
| `status` | query | `string` | no |
