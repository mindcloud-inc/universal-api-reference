# Create Conversion with CoinGate

Creates a new currency conversion in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/ledger/conversions`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Conversion](https://developer.coingate.com/reference/create-conversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ledger_account_id` | body | `string` | yes | CoinGate ledger account ID. |
| `quote_currency_id` | body | `number` | yes | CoinGate quote currency ID. |
| `base_amount` | body | `string` | yes | Conversion base amount. |
