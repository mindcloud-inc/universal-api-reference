# Update Document with fynk

Updates an existing document in fynk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Update Document](https://app.fynk.com/v1/docs#/operations/v1.documents.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `name` | body | `string` | no | Updated document name. |
