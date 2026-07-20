# Send WhatsApp template message with Tellephant

Sends a WhatsApp template message through Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send-message`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Send WhatsApp template message](https://app.tellephant.com/api-documentation#template-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `number` | yes | Recipient phone number with country code. |
| `whatsapp` | body | `object` | yes | WhatsApp template payload object from Tellephant docs. |
| `destination_url` | body | `string` | no | Optional destination URL for dynamic CTA redirect or click tracking templates. |
