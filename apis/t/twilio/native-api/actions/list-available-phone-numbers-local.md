# List Available Phone Numbers Local with Twilio

Finds available local phone numbers in Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode/Local.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Available Phone Numbers Local](https://www.twilio.com/docs/phone-numbers/api/availablephonenumberlocal-resource#read-multiple-availablephonenumberlocal-resources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CountryCode` | path | `string` | yes |
| `AreaCode` | query | `string` | no |
| `Contains` | query | `string` | no |
