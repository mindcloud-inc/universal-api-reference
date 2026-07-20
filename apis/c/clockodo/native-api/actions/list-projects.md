# List Projects with Clockodo

Retrieves projects from your Clockodo account.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [List Projects](https://www.clockodo.com/en/api/projects/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter[active]` | query | `boolean` | no |
| `filter[customers_id]` | query | `string` | no |
