# Update Currency Rates with SalesDrive

Updates current currency rates in SalesDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/currencies/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Update Currency Rates](https://api.salesdrive.me/api/docs/#/currency/currency-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currencies[]` | body | `array<object>` | yes | Array of currency rates. |
