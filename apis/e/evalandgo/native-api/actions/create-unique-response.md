# Create Unique Response with Evalandgo

Creates a unique response in Evalandgo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/responses/unique`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Create Unique Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1unique/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `respondent` | body | `string` | yes |
| `question` | body | `string` | yes |
| `choice` | body | `string` | yes |
| `text` | body | `string` | no |
