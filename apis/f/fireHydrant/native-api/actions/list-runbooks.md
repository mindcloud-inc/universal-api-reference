# List Runbooks with FireHydrant

Retrieves runbooks from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/runbooks`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Runbooks](https://docs.firehydrant.com/reference/list_runbooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter runbooks by name. |
| `owners` | query | `string` | no | Filter runbooks by owner IDs. |
| `sort` | query | `string` | no | Sort order for runbooks. |
