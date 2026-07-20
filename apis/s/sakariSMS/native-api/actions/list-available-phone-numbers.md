# List Available Phone Numbers with Sakari SMS

Finds available phone numbers in Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/availablephonenumbers`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Available Phone Numbers](https://developer.sakari.io/api-reference/availablephonenumbers/check-all-available-phone-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Phone number type |
| `postalCode` | query | `string` | no | Postal code for Number |
| `features` | query | `string` | no | Features for phone number |
| `contains` | query | `string` | no | What should be in the string |
| `areaCode` | query | `string` | no | Area Code for phone number |
| `areaCode` | query | `string` | no | Area Code for phone number |
