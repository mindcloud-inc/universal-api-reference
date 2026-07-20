# Update Multiple Response with Evalandgo

Updates an existing multiple response in Evalandgo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/responses/multiple/:id`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Update Multiple Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1multiple~1{id}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `choices[]` | body | `array<string>` | yes |
| `text` | body | `string` | no |
