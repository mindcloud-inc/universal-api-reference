# Unlink Documents with fynk

Deletes a linked document relationship from fynk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents/:document/linked-documents/:documentRelationship`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Unlink Documents](https://app.fynk.com/v1/docs#/operations/v1.documents.linked-documents.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `documentRelationship` | path | `string` | no | Document relationship UUID. |
