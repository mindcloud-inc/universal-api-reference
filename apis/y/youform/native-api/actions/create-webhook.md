# Create Webhook with Youform

Creates a webhook in Youform.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.youform.com/api`
- **Official documentation:** [Create Webhook](https://youform.com/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | query | `string` | yes | Slug of the form to create the webhook for. The provider expects this value in the `form_id` query parameter. |
| `webhook_url` | query | `string` | yes | HTTPS endpoint that should receive webhook deliveries. |
