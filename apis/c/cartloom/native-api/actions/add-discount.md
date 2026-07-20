# Add Discount with Cartloom

Creates a new discount in Cartloom.

## Endpoint

- **Method:** `POST`
- **Path:** `/discounts/add/format/json`
- **Base URL:** `https://mindcloudstage0424.cartloom.com/api`
- **Official documentation:** [Add Discount](https://support.cartloom.com/hc/en-us/articles/115000892927-Add-Discount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `list` | yes | Whether the discount is enabled. Use 1 for enabled or 0 for disabled. Accepted values: `0`, `1`. |
| `auto` | body | `list` | yes | Whether the discount applies automatically. Use 1 or 0. Accepted values: `0`, `1`. |
| `type` | body | `list` | yes | Discount type: fixed or percent. Accepted values: `0`, `1`. |
| `unlimited` | body | `list` | yes | Whether redemption is unlimited. Use 1 or 0. Accepted values: `0`, `1`. |
| `amount` | body | `number` | yes | Discount amount as a fixed amount or percentage. |
| `target` | body | `list` | yes | Discount target: product, total, or all. Accepted values: `0`, `1`, `2`. |
| `start_date` | body | `date` | yes | Start date in YYYY-MM-DD format. |
| `stop_date` | body | `date` | yes | Stop date in YYYY-MM-DD format. |
| `code` | body | `string` | no | Code customers enter to get the discount. |
| `target_pid` | body | `string` | no | Target product ID or IDs for product-targeted discounts. |
| `target_amount` | body | `number` | no | Amount required to trigger the discount. |
| `target_quantity` | body | `number` | no | Quantity required to trigger the discount. |
| `allowance` | body | `number` | no | Maximum number of times the discount can be redeemed. |
