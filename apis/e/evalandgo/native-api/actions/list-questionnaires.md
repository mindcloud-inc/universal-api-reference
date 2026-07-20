# List Questionnaires with Evalandgo

Retrieves questionnaires from Evalandgo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/questionnaires`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [List Questionnaires](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questionnaires/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | no |
| `active` | query | `boolean` | no |
| `blocked` | query | `boolean` | no |
| `visible` | query | `boolean` | no |
| `order[createAt]` | query | `string` | no |
| `order[id]` | query | `string` | no |
