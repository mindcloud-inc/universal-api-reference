# Charge Token with Skyfire

Creates a new token charge in Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens/charge`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Charge Token](https://docs.skyfire.xyz/reference/charge-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | The complete, signed JWT string received from the buyer agent in your API call. |
| `chargeAmount` | body | `string` | no | The amount to charge from the token. |
