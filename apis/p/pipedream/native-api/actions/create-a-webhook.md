# Create a webhook with Pipedream

Creates a new webhook in Pipedream.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Create a webhook](https://pipedream.com/docs/rest-api/api-reference/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | yes | The description to assign to the webhook. |
| `name` | query | `string` | yes | The name to assign to the webhook. |
| `url` | query | `string` | yes | The HTTP or HTTPS endpoint URL where events should be delivered. |
