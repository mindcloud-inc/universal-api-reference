# Update Webhook with Flexmail

Updates an existing webhook in Flexmail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/{id}`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Update Webhook](https://api.flexmail.eu/documentation/#patch-/webhooks/-id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `target_url` | body | `string` | yes |
