# Send SMS Message with Chatvolt AI

Sends an SMS message through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/twilio/{ownerPhone}/{contactPhone}/message`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send SMS Message](https://docs.chatvolt.ai/api-reference/endpoint/twilio/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownerPhone` | path | `string` | yes | The Twilio phone number that owns the integration. |
| `contactPhone` | path | `string` | yes | Recipient's phone number. |
| `message` | body | `string` | no | Textual content of the message. |
