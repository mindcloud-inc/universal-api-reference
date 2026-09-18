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

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `To` | query | `string` | no | Filter by recipient phone number in E.164 format. |
| `From` | query | `string` | no | Filter by sender phone number or sender address. |
| `DateSent` | query | `string` | no | Filter messages sent on this GMT date (YYYY-MM-DD). |
| `DateSent<` | query | `string` | no | Return messages sent on or before this GMT date (YYYY-MM-DD). |
| `DateSent>` | query | `string` | no | Return messages sent on or after this GMT date (YYYY-MM-DD). |
