# List Messaging Service Destination Alpha Senders with Twilio

Retrieves messaging service destination alpha senders from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `https://messaging.twilio.com/v1/Services/:ServiceSid/DestinationAlphaSenders`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Messaging Service Destination Alpha Senders](https://www.twilio.com/docs/messaging/api/destination-alphasender-resource#retrieve-a-list-of-destinationalphasenders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ServiceSid` | path | `string` | yes |
