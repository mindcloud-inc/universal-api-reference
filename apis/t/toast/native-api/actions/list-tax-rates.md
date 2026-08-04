# List Tax Rates with Toast

Retrieves tax rates configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/taxRates`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Tax Rates](https://doc.toasttab.com/openapi/configuration/operation/taxRatesGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
