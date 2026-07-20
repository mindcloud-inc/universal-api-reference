# Send User Deletion Email with LoginRadius

Sends a user deletion email from LoginRadius.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/identity/v2/auth/account`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Send User Deletion Email](https://www.loginradius.com/docs/api/openapi/deleteccountbyaccesstoken/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token of the user requesting account deletion email. |
| `emailtemplate` | query | `string` | no | Optional LoginRadius email template name for the deletion message. |
| `deleteurl` | query | `string` | no | Optional delete confirmation URL included in the deletion email. |
