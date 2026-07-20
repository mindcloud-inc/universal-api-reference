# Create Estimate with SWELLEnterprise

Creates a new estimate in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/finance/estimates`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Estimate](https://dashboard.swellsystem.com/docs#finance-estimates-POSTapi-v1-finance-estimates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | no | The contact ID. |
| `company_id` | body | `number` | no | The company ID. |
| `status` | body | `string` | no | The estimate status. |
| `valid_until` | body | `date` | no | The expiration date. |
| `subtotal` | body | `number` | no | The subtotal amount. |
| `tax_rate` | body | `number` | no | The tax rate percentage. |
| `currency` | body | `string` | no | The currency code. |
| `notes` | body | `string` | no | Additional notes. |
