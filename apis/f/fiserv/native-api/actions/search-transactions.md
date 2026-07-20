# Search Transactions with Fiserv

Finds transactions in Fiserv by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/search`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Search Transactions](https://isvportal.fiserv.com/docs/payments-api#operation/search_transactions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `root_source_id` | body | `string` | no | Root source ID such as payment, refund, or dispute ID. |
| `source_type` | body | `list` | no | Transaction source type filter. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `settlement_status` | body | `list` | no | Settlement status filter. Accepted values: `0`, `1`. |
| `created_at_start` | body | `date` | no | Start of created_at date-time range. |
| `created_at_end` | body | `date` | no | End of created_at date-time range. |
| `sort_column` | body | `list` | no | Sort column. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `sort_direction` | body | `list` | no | Sort direction. Accepted values: `0`, `1`. |
| `amount_min` | body | `number` | no | Minimum transaction amount. |
| `amount_max` | body | `number` | no | Maximum transaction amount. |
| `limit` | body | `number` | no | Maximum number of rows. Official max is 50. |
| `page` | body | `number` | no | Page number, starting at 1. |
