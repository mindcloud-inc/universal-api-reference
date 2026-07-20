# List Folders with Zoho Mail

Retrieves all folders from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [List Folders](https://www.zoho.com/mail/help/api/get-all-folder-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier returned by List Accounts. |
