# Update Webhook with JetAPI

Updates an existing webhook in JetAPI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/webhooks/:id`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Update Webhook](https://docs.jetapi.io/#96d9833d-7367-4b14-9d8c-a152360e608a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The JetAPI webhook identifier. |
| `types[]` | query | `array<string>` | yes | Updated list of webhook events. |
| `url` | query | `string` | yes | The updated address to which the notification is sent. |
