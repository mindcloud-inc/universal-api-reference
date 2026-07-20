# List Functions with Cradl AI

Retrieves all functions from Cradl AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/functions`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [List Functions](https://docs.cradl.ai/api-reference/get-functions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | query | `string` | no | Owner filter for functions. |
| `sortBy` | query | `string` | no | Field to sort functions by. |
| `order` | query | `string` | no | Sort order. |
