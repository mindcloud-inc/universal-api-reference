# Test Webhook with Buttondown

Sends a test event to a Buttondown webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:id/test`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Test Webhook](https://docs.buttondown.com/api-webhooks-test)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID. |
