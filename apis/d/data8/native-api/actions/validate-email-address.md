# Validate Email Address with Data8

Validates an email address with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/EmailValidation/IsValid.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Validate Email Address](https://docs.data-8.co.uk/web-services/emailvalidation/isvalid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to validate. |
| `level` | body | `string` | yes | The validation level to apply. |
| `options` | body | `object` | no | Optional settings that control email validation behavior. |
