# List Sales Order Tickets Without Refunds with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `alt-slsmg/sales/{sales_order_id}/tickets`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [List Sales Order Tickets Without Refunds](https://developer.sky.blackbaud.com/api#api=alt-slsmg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sales_order_id` | path | `string` | yes | The Blackbaud sales order identifier. |
| `limit` | query | `number` | no | Maximum number of rows to return. |
| `session_key` | query | `string` | no | Paging session key returned by Blackbaud for multi-page reads. |
| `infinity_session` | query | `string` | no | Blackbaud Infinity session identifier when required by the endpoint. |
| `more_rows_range_key` | query | `string` | no | Blackbaud cursor-like range key for additional rows. |
| `start_row_index` | query | `number` | no | Row index to start returning results from. |
