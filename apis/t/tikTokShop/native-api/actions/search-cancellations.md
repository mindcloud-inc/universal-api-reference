# Search Cancellations with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `/return_refund/202602/cancellations/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Search Cancellations](https://partner.tiktokshop.com/docv2/page/search-cancellations-202602)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `string` | yes | — |
| `cancel_ids[]` | body | `array<string>` | no | — |
| `order_ids[]` | body | `array<string>` | no | — |
| `buyer_user_ids[]` | body | `array<string>` | no | — |
| `cancel_types` | body | `list<string>` | no | Accepted values: `BUYER_CANCEL`, `CANCEL`. Send multiple values as a array. |
| `cancel_status` | body | `list<string>` | no | Accepted values: `CANCELLATION_REQUEST_CANCEL`, `CANCELLATION_REQUEST_COMPLETE`, `CANCELLATION_REQUEST_PENDING`, `CANCELLATION_REQUEST_SUCCESS`. Send multiple values as a array. |
| `create_time_ge` | body | `date` | no | — |
| `create_time_lt` | body | `date` | no | — |
| `update_time_ge` | body | `date` | no | — |
| `update_time_lt` | body | `date` | no | — |
| `locale` | body | `string` | no | — |
| `sort_field` | query | `list<string>` | no | Accepted values: `create_time`, `update_time`. |
| `sort_order` | query | `list<string>` | no | Accepted values: `ASC`, `DESC`. |
