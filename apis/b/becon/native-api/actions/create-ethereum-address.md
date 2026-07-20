# Create Ethereum Address with Becon

Creates a new Ethereum payment address in Becon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/address`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Create Ethereum Address](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | body | `string` | yes | Fixed target network for this preset. |
| `external_id` | body | `string` | yes | Unique tracking value returned in callbacks. |
| `origin_amount` | body | `string` | yes | Amount in the origin currency for automatic conversion. |
| `origin_currency` | body | `string` | yes | Origin fiat currency, for example USD or EUR. |
| `payment_currency` | body | `string` | yes | Token ticker to accept, for example ETH or USDC. |
