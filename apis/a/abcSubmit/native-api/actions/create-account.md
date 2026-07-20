# Create Account with AbcSubmit

Creates a new AbcSubmit account.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/users/create-account`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Create Account](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_name` | body | `string` | yes | The username for the new AbcSubmit account. |
| `email` | body | `string` | yes | The email address for the new AbcSubmit account. |
| `first_name` | body | `string` | yes | The first name for the new account. |
| `last_name` | body | `string` | yes | The last name for the new account. |
| `password` | body | `string` | yes | The password for the new AbcSubmit account. |
| `confirm_password` | body | `string` | yes | Repeat the password for confirmation. |
