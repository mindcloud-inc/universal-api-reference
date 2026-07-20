# Delete Webhook with Myphoner

Deletes a webhook subscription from Myphoner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhook/:webhookId`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Delete Webhook](https://www.myphoner.com/docs/api/#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `number` | yes | The Myphoner webhook ID. |
