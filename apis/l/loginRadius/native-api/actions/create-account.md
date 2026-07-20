# Create Account with LoginRadius

Creates a new account in LoginRadius.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/v2/manage/account`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Create Account](https://www.loginradius.com/docs/api/openapi/create-user/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Primary email address for the new account. |
| `password` | body | `string` | yes | Password for the new account. |
