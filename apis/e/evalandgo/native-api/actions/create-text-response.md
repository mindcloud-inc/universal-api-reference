# Create Text Response with Evalandgo

Creates a text response in Evalandgo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/responses/text`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Create Text Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1text/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `respondent` | body | `string` | yes |
| `question` | body | `string` | yes |
| `text` | body | `string` | yes |
