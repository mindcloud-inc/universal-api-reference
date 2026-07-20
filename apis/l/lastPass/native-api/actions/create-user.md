# Create User with LastPass

Creates a new user in LastPass.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterpriseapi.php`
- **Base URL:** `https://lastpass.com`
- **Official documentation:** [Create User](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
| `password` | body | `string` | yes |
| `password_reset_required` | body | `boolean` | no |
