# Update Webhook with Resend

Updates an existing webhook in Resend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Update Webhook](https://resend.com/docs/api-reference/webhooks/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<string>` | yes | The unique identifier of the webhook to update |
| `endpoint` | body | `string` | no | The URL where webhook events will be sent |
| `events[]` | body | `array<string>` | no | Array of event types to subscribe to |
