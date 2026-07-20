# List Question Responses with Evalandgo

Retrieves responses for a question from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/questions/:questionId/responses`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [List Question Responses](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questions~1{questionId}~1responses/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `questionId` | path | `string` | yes |
| `id` | query | `string` | no |
| `respondent` | query | `string` | no |
