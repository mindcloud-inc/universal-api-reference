# List Environments with FireHydrant

Retrieves environments from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Environments](https://docs.firehydrant.com/reference/list_environments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter environments by name. |
| `query` | query | `string` | no | Search environments by name. |
