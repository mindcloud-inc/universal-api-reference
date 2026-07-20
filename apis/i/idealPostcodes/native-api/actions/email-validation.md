# Email Validation with Ideal Postcodes

Validates an email address in Ideal Postcodes.

## Endpoint

- **Method:** `GET`
- **Path:** `/emails`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Email Validation](https://docs.ideal-postcodes.co.uk/docs/api/email-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Email address to validate. |
| `tags` | query | `string` | no | Comma-separated tags to associate with the validation request. |
