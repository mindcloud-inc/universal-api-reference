# Retrieve Respondent Response with Evalandgo

Retrieves a response for a respondent from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/respondents/:respondentId/responses/:id`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Retrieve Respondent Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1respondents~1{respondentId}~1responses~1{id}/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `respondentId` | path | `string` | yes |
| `id` | path | `string` | yes |
