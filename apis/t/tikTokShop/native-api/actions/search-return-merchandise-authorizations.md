# Search Return Merchandise Authorizations with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `/return_refund/202604/rma/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Search Return Merchandise Authorizations](https://partner.tiktokshop.com/docv2/page/search-return-merchandise-authorizations-202604)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `string` | yes | — |
| `locale` | query | `string` | no | — |
| `whitelisted_data_fields` | body | `list<string>` | no | Accepted values: `LINE_ITEMS`, `SKU_RETURN_REQUESTS`. Send multiple values as a array. |
| `filters` | body | `object` | no | — |
| `filters.rma_ids[]` | body | `array<string>` | no | — |
| `filters.package_ids[]` | body | `array<string>` | no | — |
| `filters.statuses` | body | `list<string>` | no | Accepted values: `AWAITING_BUYER_RETURN`, `INIT`, `PACKAGE_REVIEW_COMPLETED`, `PENDING_PACKAGE_REVIEW`, `RETURN_IN_TRANSIT`. Send multiple values as a array. |
| `filters.aftersales_request_ids[]` | body | `array<string>` | no | — |
| `filters.main_order_ids[]` | body | `array<string>` | no | — |
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
