# List All Texts with JustCall

Retrieves texts from JustCall.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2.1/texts`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [List All Texts](https://developer.justcall.io/reference/texts_list_v21)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `from_datetime` | query | `string` | no |
| `to_datetime` | query | `string` | no |
| `last_sms_id_fetched` | query | `number` | no |
| `contact_number` | query | `string` | no |
| `justcall_number` | query | `string` | no |
| `sms_direction` | query | `string` | no |
| `sms_content` | query | `string` | no |
| `sort` | query | `string` | no |
| `order` | query | `string` | no |
