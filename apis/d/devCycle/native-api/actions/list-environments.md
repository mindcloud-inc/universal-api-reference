# List Environments with DevCycle

Retrieves environments from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/environments`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Environments](https://docs.devcycle.com/management-api/#tag/Environments/operation/EnvironmentsController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Project key or ID. |
| `page` | query | `number` | no | Page number starting at 1. |
| `perPage` | query | `number` | no | Maximum items to return, up to 1000. |
| `sortBy` | query | `string` | no | Field to sort by. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `sortOrder` | query | `string` | no | Sort direction. Accepted values: `0`, `1`. |
| `search` | query | `string` | no | Search term with minimum length 3. |
| `createdBy` | query | `string` | no | Filter by creator user ID. |
