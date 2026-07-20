# List Estimates with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [List Estimates](https://www.zoho.com/books/api/v3/estimates/#list-estimates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list` | yes | — |
| `estimate_number` | query | `string` | no | — |
| `reference_number` | query | `string` | no | — |
| `customer_name` | query | `string` | no | — |
| `total` | query | `number` | no | — |
| `customer_id` | query | `list` | no | — |
| `item_id` | query | `list` | no | — |
| `item_name` | query | `string` | no | — |
| `item_description` | query | `string` | no | — |
| `custom_field` | query | `string` | no | — |
| `expiry_date` | query | `string` | no | — |
| `date` | query | `date` | no | — |
| `status` | query | `list` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `filter_by` | query | `list` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `search_text` | query | `string` | no | — |
| `zcrm_potential_id` | query | `number` | no | — |
