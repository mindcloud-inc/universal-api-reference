# Start SMS Conversation with WotNot

Creates an SMS conversation in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversations`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Start SMS Conversation](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Configured SMS sender phone number |
| `to.phone` | body | `string` | yes | Recipient phone number |
| `to.name` | body | `string` | no | Recipient display name |
| `to.email` | body | `string` | no | Recipient email |
| `message.text` | body | `string` | yes | SMS body text |
| `assignee` | body | `string` | yes | Agent email to assign the conversation to |
