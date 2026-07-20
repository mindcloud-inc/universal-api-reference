# Send File with JetAPI

Creates a new file delivery in JetAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/send_file`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Send File](https://docs.jetapi.io/#2527e2f5-c9be-4925-8657-a76116267816)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Public URL or file payload to send. |
| `file_name` | query | `string` | yes | File name including extension. |
| `phone` | query | `string` | yes | Recipient phone number in international format. |
| `caption` | query | `string` | no | — |
| `customer_id` | query | `string` | no | — |
| `type` | query | `string` | no | — |
| `sender_name` | query | `string` | no | — |
| `utm_mark` | query | `string` | no | — |
| `callback_url` | query | `string` | no | — |
| `external_id` | query | `string` | no | — |
| `dispatch_routing[]` | query | `array<string>` | no | — |
| `scheduled_at` | query | `date` | no | — |
| `priority` | query | `string` | no | — |
| `username` | query | `string` | no | — |
| `reply_to_message_id` | query | `string` | no | — |
| `tdlib_user_id` | query | `string` | no | — |
| `simulate_typing` | query | `boolean` | no | — |
