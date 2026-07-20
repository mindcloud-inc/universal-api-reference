# List Messaging Service Alpha Senders with Twilio

Retrieves messaging service alpha senders from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `https://messaging.twilio.com/v1/Services/:ServiceSid/AlphaSenders`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Messaging Service Alpha Senders](https://www.twilio.com/docs/messaging/api/alphasender-resource#retrieve-a-list-of-alphasenders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ServiceSid` | path | `string` | yes |
