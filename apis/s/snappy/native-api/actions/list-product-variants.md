# List Product Variants with Snappy

Retrieves variants for a product from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{productId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [List Product Variants](https://docs.snappy.com/reference/getvariantsbyproductid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | Product ID. |
| `minBudget` | query | `number` | no | Minimum budget. |
| `maxBudget` | query | `number` | no | Maximum budget. |
| `companyId` | query | `string` | no | Company ID. |
| `country` | query | `string` | no | Country. |
| `accountId` | query | `string` | no | Account ID. |
| `fields[]` | query | `array<string>` | no | Additional variant fields to include. |
