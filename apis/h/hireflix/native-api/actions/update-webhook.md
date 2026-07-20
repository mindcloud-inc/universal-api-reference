# Update Webhook with Hireflix

Updates an existing webhook in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Update Webhook](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix webhook ID. |
| `variables.url` | body | `string` | no | The destination URL for webhook deliveries. |
| `variables.events` | body | `string` | no | The webhook event types to subscribe to. Send multiple values as a array. |
| `variables.active` | body | `boolean` | no | Whether the webhook should remain active. |
