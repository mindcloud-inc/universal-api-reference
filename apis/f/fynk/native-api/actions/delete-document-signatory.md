# Delete Document Signatory with fynk

Deletes a document signatory from fynk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents/:document/signatories/:signatory`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Delete Document Signatory](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `signatory` | path | `string` | no | Signatory UUID. |
