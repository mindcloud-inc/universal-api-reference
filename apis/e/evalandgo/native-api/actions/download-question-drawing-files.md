# Download Question Drawing Files with Evalandgo

Retrieves drawing files for a question from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/questions/drawing/:id/download/:format`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Download Question Drawing Files](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questions~1drawing~1{id}~1download~1{format}/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `format` | path | `string` | yes |
