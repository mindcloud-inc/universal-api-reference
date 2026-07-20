# List Projects with Harpoon

Retrieves projects from Harpoon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [List Projects](https://app.harpoonapp.com/api)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select` | query | `string` | no | If present, returns simplified data for dropdowns. |
| `status` | query | `string` | no | Filter by project status. |
| `type` | query | `string` | no | Filter by project type. |
| `client_id` | query | `number` | no | Filter by client ID. |
| `search` | query | `string` | no | Search projects by name, type, status, or client. |
