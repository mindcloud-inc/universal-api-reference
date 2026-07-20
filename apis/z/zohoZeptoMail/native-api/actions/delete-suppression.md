# Delete Suppression with Zoho ZeptoMail

Deletes a suppression list entry from Zoho ZeptoMail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `suppressions/:type`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Delete Suppression](https://www.zoho.com/zeptomail/help/api/delete-suppression-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Suppression category to manage. |
| `values[0]` | body | `string` | yes | Email address or domain to remove from suppression. |
