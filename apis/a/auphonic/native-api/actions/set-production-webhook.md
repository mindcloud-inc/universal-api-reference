# Set Production Webhook with Auphonic

Sets a production webhook in Auphonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/production/:uuid/webhook.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Set Production Webhook](https://auphonic.com/help/api/webhook.html#add-a-webhook-to-a-production)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the production. |
| `webhook` | body | `string` | yes | Webhook callback URL. |
