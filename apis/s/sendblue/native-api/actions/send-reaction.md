# Send Reaction with Sendblue

Sends an iMessage reaction through Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/send-reaction`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Send Reaction](https://docs.sendblue.com/api-v2/reactions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_number` | body | `string` | yes | Your Sendblue line number in E.164 format. |
| `message_handle` | body | `string` | yes | The inbound webhook message_handle value to react to. |
| `reaction` | body | `string` | yes | The tapback reaction to send. |
| `part_index` | body | `number` | no | The zero-based part index for a multi-part message. |
