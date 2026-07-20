# Move Document To Done Stage with fynk

Moves a document to the done stage in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/stage-transitions/done`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Move Document To Done Stage](https://app.fynk.com/v1/docs#/operations/v1.documents.stage-transitions.done)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | yes | Document UUID. |
