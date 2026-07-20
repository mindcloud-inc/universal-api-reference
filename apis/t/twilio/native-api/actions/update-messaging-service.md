# Update Messaging Service with Twilio

Updates an existing messaging service in Twilio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://messaging.twilio.com/v1/Services/:Sid`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [Update Messaging Service](https://www.twilio.com/docs/messaging/api/service-resource#update-a-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Sid` | path | `string` | yes | Messaging Service SID to update |
| `FriendlyName` | body | `string` | yes | Updated friendly name for the messaging service |
