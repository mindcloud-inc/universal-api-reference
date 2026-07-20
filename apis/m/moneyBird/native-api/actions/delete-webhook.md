# Delete Webhook with MoneyBird

Deletes an existing webhook from MoneyBird.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:administrationId/webhooks/:webhookId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Delete Webhook](https://developer.moneybird.com/api/webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `webhookId` | path | `string` | yes | Moneybird webhook ID. |
