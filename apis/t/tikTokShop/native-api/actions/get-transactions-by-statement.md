# Get Transactions by Statement with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `finance/:version/statements/:statement_id/statement_transactions`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Transactions by Statement](https://partner.tiktokshop.com/docv2/page/get-statements-202309)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `shop_cipher` | query | `string` | no |
| `statement_id` | path | `string` | no |
| `sort_field` | query | `string` | no |
| `version` | path | `string` | no |
