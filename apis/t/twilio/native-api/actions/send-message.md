# Send Message with Twilio

Sends a new message with Twilio.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounts/:AccountSid/Messages.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [Send Message](https://www.twilio.com/docs/messaging/api/message-resource#create-a-message-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `To` | body | `string` | yes | Recipient phone number in E.164 format. |
| `Body` | body | `string` | yes | SMS text content. |
| `From` | body | `string` | no | Optional sender phone number or sender address. Uses the connection default when configured. |
| `MessagingServiceSid` | body | `string` | no | Optional Twilio Messaging Service SID. Leave blank unless this workflow uses a Messaging Service. |
| `StatusCallback` | body | `string` | no | Optional URL to receive Twilio message status callbacks. |
| `ValidityPeriod` | body | `number` | no | Optional maximum queue time in seconds (1-36000). |
| `SmartEncoded` | body | `boolean` | no | Replace supported Unicode characters with GSM-7 equivalents when enabled. |
| `ProvideFeedback` | body | `boolean` | no | Indicate that this workflow will provide delivery feedback to Twilio. |
