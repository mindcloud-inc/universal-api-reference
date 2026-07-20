# Send Message with Twilio

Sends a new message with Twilio.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounts/:AccountSid/Messages.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [Send Message](https://www.twilio.com/docs/messaging/api/message-resource#create-a-message-resource)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `To` | body | `string` | yes |
| `Body` | body | `string` | yes |
| `From` | body | `string` | no |
| `MessagingServiceSid` | body | `string` | no |
