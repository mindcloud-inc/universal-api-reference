# Test Webhook with Helpjuice

Tests a webhook in Helpjuice.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:id/test`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Test Webhook](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Helpjuice webhook id. |
