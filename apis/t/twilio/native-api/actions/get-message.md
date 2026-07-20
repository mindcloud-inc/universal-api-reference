# Get Message with Twilio

Retrieves a message from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts/:AccountSid/Messages/:MessageSid.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [Get Message](https://www.twilio.com/docs/messaging/api/message-resource#fetch-a-message-resource)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `MessageSid` | path | `string` | yes |
