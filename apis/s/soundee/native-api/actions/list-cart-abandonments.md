# List Cart Abandonments with Soundee

Retrieves abandoned cart records from Soundee.

## Endpoint

- **Method:** `GET`
- **Path:** `/cart-abandonments`
- **Base URL:** `https://api.soundee.com/me`
- **Official documentation:** [List Cart Abandonments](https://soundee.readme.io/reference/read-list-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_type` | query | `string` | no | Filter abandoned carts by state. |
| `q` | query | `string` | no | Search by customer name, email, token, or price. |
