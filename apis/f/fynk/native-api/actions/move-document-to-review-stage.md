# Move Document To Review Stage with fynk

Moves a document to the review stage in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/stage-transitions/review`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Move Document To Review Stage](https://app.fynk.com/v1/docs#/operations/v1.documents.stage-transitions.review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | yes | Document UUID. |
