# Get Available Phone Number Country with Twilio

Retrieves available phone number details for a country in Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [Get Available Phone Number Country](https://www.twilio.com/docs/phone-numbers/api/availablephonenumber-resource#fetch-a-specific-country)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CountryCode` | path | `string` | yes |
