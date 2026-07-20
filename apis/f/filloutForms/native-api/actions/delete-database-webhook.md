# Delete Database Webhook with Fillout Forms

Deletes a database webhook from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/webhooks/:webhookId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Delete Database Webhook](https://www.fillout.com/help/database/delete-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
| `webhookId` | path | `number` | yes | The unique identifier of the webhook. |
