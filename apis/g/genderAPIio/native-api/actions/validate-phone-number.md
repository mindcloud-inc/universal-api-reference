# Validate Phone Number with GenderAPI.io

Retrieves phone validation details from GenderAPI.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/phone`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Validate Phone Number](https://www.genderapi.io/docs-phone-validation-formatter-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | The phone number to validate in E.164, national, or international format. |
| `address` | body | `string` | no | Optional country, region, or city hint used when the number does not include an international country code. |
