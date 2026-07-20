# Update a Webhook with Linkbreakers

Updates an existing webhook in Linkbreakers.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/webhooks/:id`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Update a Webhook](https://linkbreakers.com/help/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the webhook to update. |
| `endpointUrl` | body | `string` | no | The webhook endpoint URL. |
| `linkId` | body | `string` | no | Optional link ID filter for webhook notifications. |
| `name` | body | `string` | no | The name of the webhook. |
| `source` | body | `string` | no | The source of the webhook. |
| `status` | body | `string` | no | The status of the webhook. |
| `triggers[]` | body | `array<string>` | no | Workflow step kinds that should trigger the webhook. |
