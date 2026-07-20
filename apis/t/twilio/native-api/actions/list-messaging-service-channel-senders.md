# List Messaging Service Channel Senders with Twilio

Retrieves messaging service channel senders from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `https://messaging.twilio.com/v1/Services/:ServiceSid/ChannelSenders`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Messaging Service Channel Senders](https://www.twilio.com/docs/messaging/api/messaging-service-channelsender-resource#retrieve-a-list-of-channelsenders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ServiceSid` | path | `string` | yes |
