# Disable User with LastPass

Disables an existing user in LastPass.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterpriseapi.php`
- **Base URL:** `https://lastpass.com`
- **Official documentation:** [Disable User](https://support.lastpass.com/help/lastpass-provisioning-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the user to disable. |
