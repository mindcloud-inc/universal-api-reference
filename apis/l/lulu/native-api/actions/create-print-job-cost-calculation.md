# Create Print Job Cost Calculation with Lulu

Calculates print job costs in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/print-job-cost-calculations/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Print Job Cost Calculation](https://api.lulu.com/docs/#tag/Print-Job-Cost-Calculations/operation/Print-Job-cost-calculations_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `line_items[]` | body | `array` | yes | Array of Lulu line items to price. |
| `shipping_address` | body | `object` | yes | Shipping address used for Lulu cost calculation. |
| `shipping_option` | body | `string` | yes | Lulu shipping option level. |
