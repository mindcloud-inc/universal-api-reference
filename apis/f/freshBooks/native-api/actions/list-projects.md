# List Projects with FreshBooks

Retrieves projects from FreshBooks for a business.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/business/:businessId/projects`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Projects](https://www.freshbooks.com/api/project)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
