# List Messaging Service Phone Numbers with Twilio

Retrieves messaging service phone numbers from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `https://messaging.twilio.com/v1/Services/:ServiceSid/PhoneNumbers`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Messaging Service Phone Numbers](https://www.twilio.com/docs/messaging/api/phonenumber-resource#retrieve-a-list-of-phonenumbers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ServiceSid` | path | `string` | yes |
