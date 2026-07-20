# Create a Webhook with Linkbreakers

Creates a new webhook in Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Create a Webhook](https://linkbreakers.com/help/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointUrl` | body | `string` | yes | The webhook endpoint URL. |
| `linkId` | body | `string` | no | Optional link ID filter for webhook notifications. |
| `name` | body | `string` | yes | The name of the webhook. |
| `source` | body | `string` | no | The source of the webhook. |
| `triggers[]` | body | `array<string>` | no | Workflow step kinds that should trigger the webhook. |
