# Move Document To Signing Stage with fynk

Moves a document to the signing stage in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/stage-transitions/signing`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Move Document To Signing Stage](https://app.fynk.com/v1/docs#/operations/v1.documents.stage-transitions.signing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | yes | Document UUID. |
