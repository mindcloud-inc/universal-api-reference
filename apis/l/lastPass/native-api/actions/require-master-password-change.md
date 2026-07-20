# Require Master Password Change with LastPass

Requires a LastPass user to change their master password.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterpriseapi.php`
- **Base URL:** `https://lastpass.com`
- **Official documentation:** [Require Master Password Change](https://support.lastpass.com/help/lastpass-provisioning-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the user who should be prompted to change their master password. |
