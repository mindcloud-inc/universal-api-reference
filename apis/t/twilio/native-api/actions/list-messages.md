# List Messages with Twilio

Retrieves messages from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts/:AccountSid/Messages.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Messages](https://www.twilio.com/docs/messaging/api/message-resource#read-multiple-message-resources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `To` | query | `string` | no |
| `From` | query | `string` | no |
| `DateSent` | query | `date` | no |
