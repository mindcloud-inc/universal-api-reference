# Create Webhook with Priority Matrix

Creates a new webhook in Priority Matrix.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/hook/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Create Webhook](https://sync.appfluence.com/developer/guide/#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Webhook event, for example item.created. |
| `target` | body | `string` | yes | Webhook delivery URL. |
