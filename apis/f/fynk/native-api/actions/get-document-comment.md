# Get Document Comment with fynk

Retrieves a document comment from fynk.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:document/comments/:comment`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Get Document Comment](https://app.fynk.com/v1/docs#/operations/v1.documents.comments.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | path | `string` | yes | Comment UUID. |
| `document` | path | `string` | yes | Document UUID. |
