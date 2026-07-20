# Update Text Response with Evalandgo

Updates an existing text response in Evalandgo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/responses/text/:id`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Update Text Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1text~1{id}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `text` | body | `string` | yes |
