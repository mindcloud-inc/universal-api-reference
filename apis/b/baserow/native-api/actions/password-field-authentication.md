# Password Field Authentication with Baserow

Checks a Baserow row against a password field.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/database/fields/password-authentication/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Password Field Authentication](https://api.baserow.io/api/redoc/#operation/password_field_authentication)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_id` | body | `number` | yes | The password field to check. |
| `row_id` | body | `number` | yes | The row containing the password value. |
| `password` | body | `string` | yes | The password to validate. |
