# Create Webhook with Bonusly

Creates a new webhook in Bonusly.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Create Webhook](https://docs.bonus.ly/reference/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_types` | body | `string` | no | Optional webhook event types. |
| `url` | body | `string` | yes | The webhook destination URL. |
