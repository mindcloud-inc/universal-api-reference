# List Messaging Service Short Codes with Twilio

Retrieves messaging service short codes from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `https://messaging.twilio.com/v1/Services/:ServiceSid/ShortCodes`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Messaging Service Short Codes](https://www.twilio.com/docs/messaging/api/services-shortcode-resource#retrieve-a-list-of-shortcodes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ServiceSid` | path | `string` | yes |
