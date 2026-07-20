# List Agreement Links with Harbour

Retrieves a list of agreement links from Harbour.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.harbourshare.com/v1/agreement_links`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [List Agreement Links](https://developers.harbourshare.com/#list-agreement-links)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Skip records before this offset. |
| `limit` | query | `number` | no | Limit results per response. |
| `order_by` | query | `string` | no | Sort field: ID, TITLE, or DATE_CREATED. |
| `sort_order` | query | `string` | no | Sort direction: ASC or DESC. |
