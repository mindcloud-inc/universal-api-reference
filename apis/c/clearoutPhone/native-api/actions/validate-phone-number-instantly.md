# Validate Phone Number Instantly with ClearoutPhone

Retrieves instant validation details for a phone number from ClearoutPhone.

## Endpoint

- **Method:** `POST`
- **Path:** `/phonenumber/validate`
- **Base URL:** `https://api.clearoutphone.io/v1`
- **Official documentation:** [Validate Phone Number Instantly](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-InstantPhoneNumberValidation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | A phone number to validate |
| `country_code` | body | `string` | no | Country code of phone number to be validated |
| `timeout` | body | `number` | no | Request wait time in milliseconds |
