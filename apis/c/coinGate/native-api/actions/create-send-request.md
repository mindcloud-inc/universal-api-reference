# Create Send Request with CoinGate

Creates a new send request in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_requests`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Send Request](https://developer.coingate.com/reference/create-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ledger_account_id` | body | `string` | yes | CoinGate ledger account ID. |
| `beneficiary_payout_setting_id` | body | `number` | yes | CoinGate beneficiary payout setting ID. |
| `amount` | body | `string` | yes | Send request amount. |
| `amount_currency_id` | body | `number` | yes | CoinGate amount currency ID. |
| `purpose` | body | `string` | yes | Send request purpose. |
