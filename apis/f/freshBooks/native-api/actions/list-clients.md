# List Clients with FreshBooks

Retrieves clients from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/users/clients`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Clients](https://www.freshbooks.com/api/clients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
