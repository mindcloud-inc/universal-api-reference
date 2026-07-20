# Get Webhook with Topia

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/webhooks/:webhookId`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [Get Webhook](https://api.topia.io/api-docs/paths/v1/webhook.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `webhookId` | path | `string` | yes | Identifier for the webhook. |
