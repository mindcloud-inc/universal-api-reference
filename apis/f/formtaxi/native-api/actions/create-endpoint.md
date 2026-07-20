# Create Endpoint with Form.taxi

Creates a new endpoint in Form.taxi.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-endpoint`
- **Base URL:** `https://form.taxi/api/v1`
- **Official documentation:** [Create Endpoint](https://docs.form.taxi/en/api-create-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address used as the destination for form submissions and as the username for the new account. |
| `form_name` | body | `string` | yes | Name of the form to create. |
| `language` | body | `string` | yes | Language for the account and email notifications. |
| `website_url` | body | `string` | no | Website where the form will be used. |
| `timezone` | body | `string` | no | IANA time zone identifier for the account. |
