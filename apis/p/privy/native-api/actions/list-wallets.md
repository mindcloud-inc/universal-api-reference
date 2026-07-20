# List Wallets with Privy

Retrieves a list of wallets from Privy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/wallets`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [List Wallets](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_type` | query | `string` | no | Optional wallet chain type filter. |
| `user_id` | query | `string` | no | Optional user ID filter. |
| `authorization_key` | query | `string` | no | Optional authorization key filter. |
| `external_id` | query | `string` | no | Optional external ID filter. |
