# Validate Phone Number with Data8

Validates a phone number with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/PhoneValidation/IsValid.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Validate Phone Number](https://docs.data-8.co.uk/web-services/phonevalidation/isvalid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `telephoneNumber` | body | `string` | yes | The telephone number to validate. |
| `defaultCountry` | body | `string` | no | Country code to assume when the number has no international dialling code. |
| `options` | body | `object` | no | Optional settings that control validation behavior. |
