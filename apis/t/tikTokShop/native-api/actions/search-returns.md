# Search Returns with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `/return_refund/202602/returns/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Search Returns](https://partner.tiktokshop.com/docv2/page/search-returns-202602)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `string` | yes | — |
| `return_ids[]` | body | `array<string>` | no | — |
| `order_ids[]` | body | `array<string>` | no | — |
| `buyer_user_ids[]` | body | `array<string>` | no | — |
| `return_types` | body | `list<string>` | no | Accepted values: `EXCHANGE`, `REFUND`, `REPLACEMENT`, `RETURN_AND_REFUND`. Send multiple values as a array. |
| `return_status` | body | `list<string>` | no | Accepted values: `AWAITING_BUYER_RESPONSE`, `AWAITING_BUYER_SHIP`, `BUYER_SHIPPED_ITEM`, `EXCHANGE_REQUEST_CANCEL`, `EXCHANGE_REQUEST_COMPLETE`, `EXCHANGE_REQUEST_PENDING`, `EXCHANGE_REQUEST_REFUND_SUCCESS`, `REFUND_OR_RETURN_REQUEST_REJECT`, `REJECT_RECEIVE_PACKAGE`, `REPLACEMENT_REQUEST_CANCEL`, `REPLACEMENT_REQUEST_COMPLETE`, `REPLACEMENT_REQUEST_PENDING`, `REPLACEMENT_REQUEST_REFUND_SUCCESS`, `REPLACEMENT_REQUEST_REJECT`, `RETURN_OR_REFUND_REQUEST_CANCEL`, `RETURN_OR_REFUND_REQUEST_COMPLETE`, `RETURN_OR_REFUND_REQUEST_PENDING`, `RETURN_OR_REFUND_REQUEST_SUCCESS`. Send multiple values as a array. |
| `seller_proposed_return_type` | body | `list<string>` | no | Accepted values: `PARTIAL_REFUND`. Send multiple values as a array. |
| `arbitration_status` | body | `list<string>` | no | Accepted values: `CLOSED`, `IN_PROGRESS`, `SUPPORT_BUYER`, `SUPPORT_SELLER`. Send multiple values as a array. |
| `create_time_ge` | body | `date` | no | — |
| `create_time_lt` | body | `date` | no | — |
| `update_time_ge` | body | `date` | no | — |
| `update_time_lt` | body | `date` | no | — |
| `locale` | body | `string` | no | — |
| `sort_field` | query | `list<string>` | no | Accepted values: `create_time`, `update_time`. |
| `sort_order` | query | `list<string>` | no | Accepted values: `ASC`, `DESC`. |
