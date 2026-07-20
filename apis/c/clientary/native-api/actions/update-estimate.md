# Update Estimate with Clientary

Updates an estimate in Clientary by estimate ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/estimates/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Update Estimate](https://www.clientary.com/api/estimates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate.currency_code` | body | `string` | no | The ISO currency code for the estimate. |
| `estimate.date` | body | `string` | no | The estimate issue date (YYYY-MM-DD). |
| `id` | path | `string` | yes | The Clientary estimate ID. |
