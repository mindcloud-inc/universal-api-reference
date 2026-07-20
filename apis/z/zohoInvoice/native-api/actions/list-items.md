# List Items with Zoho Invoice

Retrieves items from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/items`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [List Items](https://www.zoho.com/invoice/api/v3/items/#list-items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_text` | query | `string` | no | Maximum length: 100. |
| `name` | query | `string` | no | Maximum length: 100. |
| `name_startswith` | query | `string` | no | Maximum length: 100. |
| `name_contains` | query | `string` | no | Maximum length: 100. |
| `description` | query | `string` | no | Maximum length: 100. |
| `description_startswith` | query | `string` | no | Maximum length: 100. |
| `description_contains` | query | `string` | no | Maximum length: 100. |
| `rate` | query | `string` | no | — |
| `rate_less_than` | query | `string` | no | — |
| `rate_less_equals` | query | `string` | no | — |
| `rate_greater_than` | query | `string` | no | — |
| `rate_greater_equals` | query | `string` | no | — |
| `tax_id` | query | `string` | no | — |
| `filter_by` | query | `list<string>` | no | Accepted values: `Status.Active`, `Status.All`, `Status.Inactive`. |
