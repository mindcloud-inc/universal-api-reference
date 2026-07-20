# List Purchases with Digistore24

Retrieves a list of purchases from Digistore24.

## Endpoint

- **Method:** `GET`
- **Path:** `/listPurchases`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [List Purchases](https://digistore24.com/api/docs/paths/listPurchases.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start of the purchase time range, for example -24h. |
| `to` | query | `string` | no | End of the purchase time range, for example now. |
| `search` | query | `string` | no | Search filters |
| `sort_by` | query | `string` | no | Purchase field to sort by, such as date or purchase_id. |
| `sort_order` | query | `string` | no | Sort direction: asc or desc. |
| `load_transactions` | query | `boolean` | no | Include transaction details in the response. |
| `page_no` | query | `number` | no | Page number starting at 1. |
| `page_size` | query | `number` | no | Number of purchases per page. |
