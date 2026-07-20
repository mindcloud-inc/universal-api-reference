# Create Document From Template with fynk

Creates a new document from a template in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/create-from-template`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Create Document From Template](https://app.fynk.com/v1/docs#/operations/v1.documents.create-from-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional document name. |
| `template_uuid` | body | `string` | no | Template UUID to create the document from. |
