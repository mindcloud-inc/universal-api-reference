# Create Account with 123FormBuild

Creates a new account in 123FormBuilder when available for your account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Create Account](https://www.123formbuilder.com/developer/api-v2/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email for the account |
| `name` | body | `string` | no | Name for the account |
| `password` | body | `string` | yes | Password for the account |
| `password_repeat` | body | `string` | yes | Repeated password for confirmation |
| `plan` | body | `string` | no | Plan for the account |
| `company_name` | body | `string` | no | Company name for the account |
