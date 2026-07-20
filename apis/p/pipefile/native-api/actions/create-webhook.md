# Create Webhook with Pipefile

Creates a new webhook in Pipefile.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `https://api.pipefile.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Pipefile event that should trigger the webhook. |
| `target` | body | `string` | yes | Destination URL for webhook deliveries. |
