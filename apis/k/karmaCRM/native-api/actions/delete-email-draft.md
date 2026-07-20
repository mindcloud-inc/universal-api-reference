# Delete Email Draft with Karma CRM

Deletes an email draft from Karma CRM.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/mailman_nylas/outgoing/messages/:id.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Delete Email Draft](https://docs.karmacrm.com/#delete-an-email-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the draft email to delete. |
