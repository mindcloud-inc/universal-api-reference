# List Suppressions with Zoho ZeptoMail

Retrieves suppression list entries from Zoho ZeptoMail.

## Endpoint

- **Method:** `GET`
- **Path:** `suppressions/:type`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [List Suppressions](https://www.zoho.com/zeptomail/help/api/get-suppression-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Suppression category to manage. |
| `mailagent_keys[0]` | query | `string` | no | Filter suppression entries by agent alias. |
| `limit` | query | `number` | no | Maximum number of suppression entries to return. |
| `offset` | query | `number` | no | Number of suppression entries to skip before returning results. |
| `date_from` | query | `string` | no | Fetch entries modified on or after this date and time. |
| `date_to` | query | `string` | no | Fetch entries modified on or before this date and time. |
