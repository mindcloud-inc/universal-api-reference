# Delete Database Webhook with Fillout

Deletes a database webhook from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/webhooks/:webhookId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Delete Database Webhook](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `webhookId` | path | `string` | yes | The webhook identifier. |
