# Delete Messaging Service with Twilio

Deletes an existing messaging service from Twilio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://messaging.twilio.com/v1/Services/:Sid`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [Delete Messaging Service](https://www.twilio.com/docs/messaging/api/service-resource#delete-a-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Sid` | path | `string` | yes | Messaging Service SID to delete |
