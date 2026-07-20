# Validate Tax ID with Quaderno

Validates a tax ID in Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/tax_ids/validate`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Validate Tax ID](https://developers.quaderno.io/api/#tag/Tax-IDs/operation/validateTaxID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter ISO country code for the tax ID. |
| `tax_id` | query | `string` | no | Tax ID value to validate. |
