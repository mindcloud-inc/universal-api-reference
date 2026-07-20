# List Estimates with FreshBooks

Retrieves estimates from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/estimates/estimates`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Estimates](https://www.freshbooks.com/api/estimates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
