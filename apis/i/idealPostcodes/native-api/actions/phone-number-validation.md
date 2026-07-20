# Phone Number Validation with Ideal Postcodes

Validates a phone number in Ideal Postcodes.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone_numbers`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Phone Number Validation](https://docs.ideal-postcodes.co.uk/docs/api/phone-number-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Phone number to validate, including a country code when possible. |
| `current_carrier` | query | `boolean` | no | Set to true to request the current network carrier. |
| `tags` | query | `string` | no | Comma-separated tags to associate with the validation request. |
