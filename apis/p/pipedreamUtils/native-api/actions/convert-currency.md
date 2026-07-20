# Helper Functions - Convert Currency with Pipedream Utils

Converts an amount between currencies in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Helper Functions - Convert Currency](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/convert-currency/convert-currency.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromCurrency` | body | `string` | yes | The currency to convert from |
| `toCurrency` | body | `string` | yes | The currency to convert to |
| `value` | body | `string` | yes | The value to convert |
