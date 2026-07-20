# List Questionnaire Questions with Evalandgo

Retrieves questions for a questionnaire from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/questionnaires/:id/questions`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [List Questionnaire Questions](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questionnaires~1{id}~1questions/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Questionnaire identifier |
