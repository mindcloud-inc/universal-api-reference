# Search Aftersales Requests with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `/return_refund/202603/aftersales/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Search Aftersales Requests](https://partner.tiktokshop.com/docv2/page/search-aftersales-requests-202603)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `string` | yes | — |
| `locale` | query | `string` | no | — |
| `whitelisted_data_fields` | body | `list<string>` | no | Accepted values: `LINE_ITEMS`, `RETURN_MERCHANDISE_AUTHORIZATIONS`, `SKU_RETURN_REQUESTS`. Send multiple values as a array. |
| `filters` | body | `object` | no | — |
| `filters.aftersales_request_ids[]` | body | `array<string>` | no | — |
| `filters.aftersales_request_statuses` | body | `list<string>` | no | Accepted values: `INIT`, `PENDING_REQUEST_REVIEW`, `REQUEST_REVIEW_COMPLETED`. Send multiple values as a array. |
| `filters.return_types` | body | `list<string>` | no | Accepted values: `EXCHANGE`, `REFUND`, `REPLACEMENT`, `RETURN_AND_REFUND`. Send multiple values as a array. |
| `filters.main_order_ids[]` | body | `array<string>` | no | — |
| `filters.buyer_ids[]` | body | `array<string>` | no | — |
| `filters.time` | body | `object` | no | — |
| `filters.time.create_time` | body | `object` | no | — |
| `filters.time.create_time.min_unix_time_inclusive` | body | `date` | no | — |
| `filters.time.create_time.max_unix_time_exclusive` | body | `date` | no | — |
| `filters.time.update_time` | body | `object` | no | — |
| `filters.time.update_time.min_unix_time_inclusive` | body | `date` | no | — |
| `filters.time.update_time.max_unix_time_exclusive` | body | `date` | no | — |
| `sort` | body | `object` | no | — |
| `sort.sort_field` | body | `list<string>` | no | Accepted values: `CREATE_TIME`, `UPDATE_TIME`. |
| `sort.sort_order` | body | `list<string>` | no | Accepted values: `ASC`, `DESC`. |
