# Create Label with Zoho Mail

Creates a new label in Zoho Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/labels`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Create Label](https://www.zoho.com/mail/help/api/post-create-new-label.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier returned by List Accounts. |
| `displayName` | body | `string` | yes | Label name to create. |
| `color` | body | `string` | no | Optional label color as a hexadecimal value. |
