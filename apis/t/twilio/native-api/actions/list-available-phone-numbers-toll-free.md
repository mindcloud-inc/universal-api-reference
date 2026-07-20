# List Available Phone Numbers Toll-Free with Twilio

Finds available toll-free phone numbers in Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode/TollFree.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Available Phone Numbers Toll-Free](https://www.twilio.com/docs/phone-numbers/api/availablephonenumber-tollfree-resource#read-multiple-availablephonenumbertollfree-resources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CountryCode` | path | `string` | yes |
| `Contains` | query | `string` | no |
