# Send Transaction with Poof

Creates a new payout transaction in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `/payouts`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Send Transaction](https://docs.poof.io/reference/sendtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Payout amount. |
| `crypto` | body | `string` | yes | Crypto asset code. |
| `address` | body | `string` | yes | Destination wallet address. |
