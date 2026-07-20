# Get Exchange Rates with VAT Comply

Retrieves exchange rates from VAT Comply.

## Endpoint

- **Method:** `GET`
- **Path:** `/rates`
- **Base URL:** `https://api.vatcomply.com`
- **Official documentation:** [Get Exchange Rates](https://www.vatcomply.com/api/rates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | no | Base currency for the rates response. |
| `symbols` | query | `string` | no | Comma-separated target currency symbols. |
| `date` | query | `string` | no | Historical date for the requested exchange rates. |
