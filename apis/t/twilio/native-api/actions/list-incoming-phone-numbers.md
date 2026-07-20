# List Incoming Phone Numbers with Twilio

Retrieves incoming phone numbers from Twilio.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts/:AccountSid/IncomingPhoneNumbers.json`
- **Base URL:** `https://api.twilio.com/2010-04-01`
- **Official documentation:** [List Incoming Phone Numbers](https://www.twilio.com/docs/phone-numbers/api/incomingphonenumber-resource#read-multiple-incomingphonenumber-resources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PhoneNumber` | query | `string` | no |
| `FriendlyName` | query | `string` | no |
