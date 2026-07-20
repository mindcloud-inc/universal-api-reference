# Validate Email with ZeroBounce

Retrieves email validation details from ZeroBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/validate`
- **Base URL:** `https://api.zerobounce.net`
- **Official documentation:** [Validate Email](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-validate-emails)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `ip_address` | query | `string` | no |
| `timeout` | query | `number` | no |
| `activity_data` | query | `boolean` | no |
| `verify_plus` | query | `boolean` | no |
