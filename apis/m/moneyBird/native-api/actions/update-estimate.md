# Update Estimate with MoneyBird

Updates an existing estimate in MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/estimates/:estimateId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Update Estimate](https://developer.moneybird.com/api/estimates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `estimateId` | path | `string` | yes | Moneybird estimate ID. |
| `estimate` | body | `object` | no | — |
| `estimate.contact_id` | body | `string` | no | — |
| `estimate.reference` | body | `string` | no | — |
| `estimate.currency` | body | `string` | no | — |
| `estimate.prices_are_incl_tax` | body | `boolean` | no | — |
| `estimate.details_attributes[]` | body | `array<object>` | no | — |
| `estimate.details_attributes[].description` | body | `string` | no | — |
| `estimate.details_attributes[].amount` | body | `number` | no | — |
| `estimate.details_attributes[].price` | body | `number` | no | — |
| `estimate.details_attributes[].tax_rate_id` | body | `string` | no | — |
| `estimate.details_attributes[].ledger_account_id` | body | `string` | no | — |
| `estimate.details_attributes[].id` | body | `string` | no | — |
| `estimate.details_attributes[]._destroy` | body | `boolean` | no | — |
