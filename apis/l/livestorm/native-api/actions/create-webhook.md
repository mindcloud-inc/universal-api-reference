# Create Webhook with Livestorm

Creates a new webhook in Livestorm.

## Endpoint

- **Method:** `POST`
- **Path:** `webhooks`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Create Webhook](https://developers.livestorm.co/reference/post_webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.attributes.url` | body | `string` | no |
| `data.attributes.event` | body | `string` | no |
