# Get Current Address with Becon

Retrieves the latest payment address from Becon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/address?reset=1`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get Current Address](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | body | `string` | no | Target network: bitcoin, binance, ethereum, or tron. |
| `external_id` | body | `string` | yes | Unique tracking value returned in callbacks. |
| `origin_amount` | body | `string` | yes | Amount in the origin currency for automatic conversion. |
| `origin_currency` | body | `string` | yes | Origin fiat currency, for example USD or EUR. |
| `payment_amount` | body | `string` | no | Optional fixed payment amount to override automatic conversion. |
| `payment_currency` | body | `string` | yes | Token ticker to accept, for example USDC or BTC. |
