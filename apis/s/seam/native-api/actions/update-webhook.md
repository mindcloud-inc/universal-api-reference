# Update Webhook with Seam

Updates an existing webhook in Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/update`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Update Webhook](https://docs.seam.co/latest/api/webhooks/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_types` | body | `list<string>` | yes | Required array of webhook event types. Seam expects `event_types` as an array of strings; the current execution surface is serializing this as a string and the provider rejects the request. |
| `webhook_id` | body | `string` | yes | — |
