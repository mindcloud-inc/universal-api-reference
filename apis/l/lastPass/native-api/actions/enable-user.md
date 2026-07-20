# Enable User with LastPass

Enables an existing user in LastPass.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterpriseapi.php`
- **Base URL:** `https://lastpass.com`
- **Official documentation:** [Enable User](https://support.lastpass.com/help/lastpass-provisioning-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the user to enable. |
