# Update Webhook with Bonusly

Updates an existing webhook in Bonusly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Update Webhook](https://docs.bonus.ly/reference/update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The webhook ID. |
| `url` | body | `string` | yes | Updated webhook destination URL. |
