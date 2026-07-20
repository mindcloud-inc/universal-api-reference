# Send Typing Indicator with Sendblue

Sends an iMessage typing indicator through Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/send-typing-indicator`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Send Typing Indicator](https://docs.sendblue.com/api-v2/typing-indicators/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | The recipient phone number in E.164 format. |
| `from_number` | body | `string` | no | Your Sendblue line number in E.164 format. |
