# Create Transfer with Fintoc

Creates a transfer in Fintoc.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/transfers`
- **Base URL:** `https://api.fintoc.com`
- **Official documentation:** [Create Transfer](https://docs.fintoc.com/reference/create-transfer-outbound)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fintoc_jws_signature` | body | `string` | yes | Per-request JWS signature for transfer creation. |
| `amount` | body | `number` | yes | Transfer amount in minor units. |
| `currency` | body | `string` | yes | Transfer currency. |
| `account_id` | body | `string` | yes | Source account ID for the transfer. |
| `counterparty` | body | `object` | yes | Destination counterparty object. For MXN use at least `{ "account_number": "..." }`. |
