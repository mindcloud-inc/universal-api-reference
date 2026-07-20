# Send MMS with InflatableOffice

Sends an MMS message from InflatableOffice.

## Endpoint

- **Method:** `POST`
- **Path:** `/text`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [Send MMS](https://rental.software/support/knowledge-base/article/api-sms-text-message-sending-and-recieving)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toNumber` | body | `string` | yes | Phone number to send the message to. |
| `text` | body | `string` | yes | Text message content to send. |
| `fromNumber` | body | `string` | no | Optional IO Phone number to send from. Use (999) 999-9999 for test sends. |
| `media[]` | body | `array<string>` | yes | Media URLs to include with the message. |
