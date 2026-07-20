# List Respondent Responses with Evalandgo

Retrieves responses for a respondent from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/respondents/:respondentId/responses`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [List Respondent Responses](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1respondents~1{respondentId}~1responses/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `respondentId` | path | `string` | yes |
| `id` | query | `string` | no |
| `question` | query | `string` | no |
