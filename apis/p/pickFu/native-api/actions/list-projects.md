# List Projects with PickFu

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.pickfu.com/v1`
- **Official documentation:** [List Projects](https://www.pickfu.com/docs/api-reference/projects/list-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmarked` | query | `boolean` | no | Filter to bookmarked projects only. |
| `archived` | query | `boolean` | no | Filter to archived projects only. |
