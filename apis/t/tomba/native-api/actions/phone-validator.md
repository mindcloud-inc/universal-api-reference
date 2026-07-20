# Phone Validator with Tomba

Validates a phone number in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone-validator`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Phone Validator](https://docs.tomba.io/api/phone#phone-validator)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phone` | query | `string` | yes |
| `country_code` | query | `string` | no |
