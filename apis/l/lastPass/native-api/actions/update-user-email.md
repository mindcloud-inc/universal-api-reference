# Update User Email with LastPass

Updates a LastPass user's email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterpriseapi.php`
- **Base URL:** `https://lastpass.com`
- **Official documentation:** [Update User Email](https://support.lastpass.com/help/lastpass-provisioning-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oldEmail` | body | `string` | yes | The user's current email address. |
| `newEmail` | body | `string` | yes | The new email address to set for the user. |
