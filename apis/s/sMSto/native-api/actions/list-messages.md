# List Messages with SMS.to

Retrieves sent SMS messages from SMS.to.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/messages`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [List Messages](https://developers.sms.to/#4bcab664-aa65-4abc-b5f4-7f3037dbadcb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of messages per page. |
| `order_direction` | query | `string` | no | Sort direction. |
| `order_by` | query | `list<string>` | no | Field to sort by. Accepted fields: created_at, id, sent_at, sender_id, is_api, status, cost. Accepted values: `cost`, `created_at`, `id`, `is_api`, `sender_id`, `sent_at`, `status`. |
| `status` | query | `string` | no | Filter by status. |
| `to` | query | `string` | no | Filter by recipient number. |
| `created_at_from` | query | `date` | no | Filter from date. Format: Y-m-d H:i:s. |
| `created_at_to` | query | `date` | no | Filter to date. Format: Y-m-d H:i:s. |
