# Create Document Signatory with fynk

Creates a document signatory in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/signatories`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Create Document Signatory](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `email` | body | `string` | no | Signatory email. |
| `party_uuid` | body | `string` | no | Party UUID for the signatory. |
