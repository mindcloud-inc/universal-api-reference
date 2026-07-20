# Create Form Response with Evalandgo

Creates a form response in Evalandgo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/responses/form`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Create Form Response](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1form/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `respondent` | body | `string` | yes |
| `responseInputs[]` | body | `array<object>` | no |
| `question` | body | `string` | yes |
