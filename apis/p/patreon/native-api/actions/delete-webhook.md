# Delete Webhook with Patreon

Deletes an existing webhook from Patreon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://www.patreon.com/api/oauth2/v2`
- **Official documentation:** [Delete Webhook](https://docs.patreon.com#delete-api-oauth2-v2-webhooks-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The Patreon webhook ID. |
