# Get Daily Credit Usage with Verifalia

Retrieves daily credit usage from Verifalia.

## Endpoint

- **Method:** `GET`
- **Path:** `/credits/daily-usage`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Get Daily Credit Usage](https://verifalia.com/developers/credits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Get credit usage for one specific date in YYYY-MM-DD format. |
| `date:since` | query | `string` | no | Inclusive start date for the credit-usage period in YYYY-MM-DD format. |
| `date:until` | query | `string` | no | Inclusive end date for the credit-usage period in YYYY-MM-DD format. |
