# Update Webhook with SMASHSEND Email Marketing

Updates an existing webhook in SMASHSEND.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks/:webhookId`
- **Base URL:** `https://api.smashsend.com`
- **Official documentation:** [Update Webhook](https://smashsend.com/docs/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Updated array of SMASHSEND event names for the webhook. |
| `webhookId` | path | `string` | yes | The SMASHSEND webhook ID to update. |
