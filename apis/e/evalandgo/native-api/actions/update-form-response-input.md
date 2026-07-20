# Update Form Response Input with Evalandgo

Updates an input in a form response in Evalandgo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/responses/form/:responseId/inputs/:inputId`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Update Form Response Input](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1form~1{responseId}~1inputs~1{inputId}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `responseId` | path | `string` | yes |
| `inputId` | path | `string` | yes |
| `text` | body | `string` | no |
