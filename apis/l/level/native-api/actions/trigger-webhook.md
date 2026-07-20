# Trigger Webhook with Level

Triggers an automation webhook in Level.

## Endpoint

- **Method:** `POST`
- **Path:** `/automations/webhooks/{token}`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Trigger Webhook](https://levelapi.readme.io/reference/triggerwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `string` | yes | The token of the webhook to trigger. |
