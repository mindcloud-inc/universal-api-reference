# Update Webhook with EZICHEQ

Updates a webhook in EZICHEQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhook/v1/:id`
- **Base URL:** `https://api.ezicheq.com`
- **Official documentation:** [Update Webhook](https://developer.ezicheq.com/docs/endpoints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `url` | body | `string` | yes |
