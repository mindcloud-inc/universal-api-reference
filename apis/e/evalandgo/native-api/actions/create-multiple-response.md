# Create Multiple Response with Evalandgo

Creates a multiple response in Evalandgo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/responses/multiple`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Create Multiple Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1multiple/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `respondent` | body | `string` | yes |
| `question` | body | `string` | yes |
| `choices[]` | body | `array<string>` | yes |
| `text` | body | `string` | no |
