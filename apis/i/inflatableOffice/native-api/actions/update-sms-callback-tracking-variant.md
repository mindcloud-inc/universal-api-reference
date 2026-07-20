# Update SMS Callback Tracking Variant with InflatableOffice

Sends a text message with callback tracking from InflatableOffice.

## Endpoint

- **Method:** `POST`
- **Path:** `/text`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [Update SMS Callback Tracking Variant](https://rental.software/support/knowledge-base/article/api-sms-text-message-sending-and-recieving)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toNumber` | body | `string` | yes | Phone number to send the message to. |
| `text` | body | `string` | yes | Text message content to send. |
| `fromNumber` | body | `string` | no | Optional IO Phone number to send from. Use (999) 999-9999 for test sends. |
| `callbackUrl` | body | `string` | no | Webhook URL to receive status callbacks. |
| `customKey` | body | `string` | no | Custom tracking key returned in webhook payloads. |
