# Replace Webhook with Evalandgo

Updates an existing webhook in Evalandgo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/webhooks/:id`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Replace Webhook](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1webhooks~1{id}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `active` | body | `boolean` | no |
| `url` | body | `string` | no |
| `events[]` | body | `array<string>` | no |
