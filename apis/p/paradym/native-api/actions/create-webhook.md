# Create Webhook with Paradym

Creates a webhook in Paradym.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/webhooks`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Create Webhook](https://paradym.id/reference#tag/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A label for the webhook subscription. |
| `url` | body | `string` | yes | The public endpoint that should receive webhook events. |
