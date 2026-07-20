# Get Phone Number Scoring with Greip - Fraud Prevention

Retrieves phone number risk scoring from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/scoring/phone`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get Phone Number Scoring](https://docs.greip.io/api-reference/endpoint/scoring/phone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | The phone number to validate. |
| `countryCode` | query | `string` | yes | The ISO 3166-1 alpha-2 country code for the phone number. |
