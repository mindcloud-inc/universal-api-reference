# Preview Charge with ChargeDesk

Retrieves a charge preview from ChargeDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/preview`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Preview Charge](https://chargedesk.com/api-docs#charges-preview-charge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `charge_id` | query | `string` | no | Charge to preview. |
| `product_id` | query | `string` | no | Product to preview. Ignored if Charge ID is also provided. |
| `amount` | query | `string` | no | Amount to preview. Required if no charge or product is provided; otherwise overrides the charge or product amount. |
| `currency` | query | `string` | no | Currency to preview. Required if no charge or product is provided; otherwise overrides the charge or product currency. |
| `country` | query | `string` | no | Two-letter ISO country code for the customer location. |
| `tax_number` | query | `string` | no | Customer tax identification number used to determine whether 0% tax should apply. |
| `add_tax` | query | `boolean` | no | Override the company setting for whether tax is added to or included in the final amount. |
