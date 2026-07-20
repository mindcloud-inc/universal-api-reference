# Send Multi Messages with Wbiztool

Creates WhatsApp messages for multiple recipients in Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_msg/multi/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Send Multi Messages](https://wbiztool.com/docs/send-msg-multi-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msg_type` | body | `string` | yes | Wbiztool message type code as numeric text: 0 text, 1 image, 2 file. |
| `phone` | body | `string` | yes | Comma-separated list of phone numbers or group names to message. |
| `country_code` | body | `string` | no | Country code applied to recipient phone numbers when needed. |
| `msg` | body | `string` | yes | Message text or caption to send. |
| `img_url` | body | `string` | no | Public image URL for image campaigns. |
| `file_url` | body | `string` | no | Public file URL for file campaigns. |
| `file_name` | body | `string` | no | Optional display name for file campaigns. |
| `webhook` | body | `string` | no | Optional webhook URL to receive delivery events. |
