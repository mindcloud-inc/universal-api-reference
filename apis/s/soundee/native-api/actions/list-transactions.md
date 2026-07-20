# List Transactions with Soundee

Retrieves your transaction records from Soundee.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://api.soundee.com/me`
- **Official documentation:** [List Transactions](https://soundee.readme.io/reference/get-2)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_type` | query | `string` | no | Filter transactions by type. |
| `q` | query | `string` | no | Search by item, customer, collaborator, amount, email, or transaction ID. |
