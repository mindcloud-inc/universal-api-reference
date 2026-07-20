# Create Estimate with Clientary

Creates a new estimate in Clientary.

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Create Estimate](https://www.clientary.com/api/estimates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate.currency_code` | body | `string` | yes | The ISO currency code for the estimate. |
| `estimate.date` | body | `string` | yes | The estimate issue date (YYYY-MM-DD). |
