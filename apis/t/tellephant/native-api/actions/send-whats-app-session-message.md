# Send WhatsApp session message with Tellephant

Sends a WhatsApp session message through Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send-message`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Send WhatsApp session message](https://app.tellephant.com/api-documentation#session-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `number` | yes | Recipient phone number with country code. |
| `whatsapp` | body | `object` | yes | WhatsApp session message payload object from Tellephant docs. |
