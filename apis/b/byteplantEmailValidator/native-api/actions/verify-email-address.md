# Verify Email Address with Byteplant Email Validator

Retrieves email deliverability details from Byteplant Email Validator.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/verify`
- **Base URL:** `https://api.email-validator.net`
- **Official documentation:** [Verify Email Address](https://www.byteplant.com/email-validator/api.html#email-validation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EmailAddress` | query | `string` | yes | Email address to validate. |
| `Timeout` | query | `number` | no | Timeout in seconds (default 10, min 5, max 300). |
