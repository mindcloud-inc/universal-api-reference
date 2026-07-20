# Delete Form Webhook with Jotform

Deletes an existing form webhook from Jotform.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/form/:formId/webhooks/:webhookId`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [Delete Form Webhook](https://api.jotform.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Form ID |
| `webhookId` | path | `string` | yes | Webhook ID |
