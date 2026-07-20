# List Brands with Harbour

Retrieves a list of brands from Harbour.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.harbourshare.com/v1/organizations/brands`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [List Brands](https://developers.harbourshare.com/#list-brands)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Skip records before this offset. |
| `order_by` | query | `string` | no | Sort field: ID, TITLE, or DATE_CREATED. |
| `limit` | query | `number` | no | Limit results per response. |
| `sort_order` | query | `string` | no | Sort direction: ASC or DESC. |
