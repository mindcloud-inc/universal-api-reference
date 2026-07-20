# Create Webhook with Voog

Creates a new webhook in the current Voog site.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Webhook](https://www.voog.com/developers/api/resources/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Webhook event name. |
| `target` | body | `string` | yes | Webhook target object. |
| `url` | body | `string` | yes | Destination URL for webhook delivery. |
