# Create Billing Request with CoinGate

Creates a new billing request in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/requests`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Billing Request](https://developer.coingate.com/reference/create-billing-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_contact_id` | body | `number` | yes | CoinGate billing contact ID. |
| `currency_id` | body | `number` | yes | CoinGate currency ID. |
| `receive_currency_id` | body | `number` | yes | CoinGate receive currency ID. |
