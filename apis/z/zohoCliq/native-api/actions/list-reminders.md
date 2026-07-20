# List Reminders with Zoho Cliq

Retrieves all reminders from Zoho Cliq.

## Endpoint

- **Method:** `GET`
- **Path:** `/reminders`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Reminders](https://www.zoho.com/cliq/help/restapi/v2/#list_all_reminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | The reminder category to retrieve, such as mine. |
| `limit` | query | `number` | no | The number of reminders to retrieve. |
| `next_set_token` | query | `string` | no | Use the token from a previous response to retrieve the next reminder page. |
