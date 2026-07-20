# Update Unique Response with Evalandgo

Updates an existing unique response in Evalandgo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/responses/unique/:id`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Update Unique Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1unique~1{id}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `choice` | body | `string` | yes |
| `text` | body | `string` | no |
