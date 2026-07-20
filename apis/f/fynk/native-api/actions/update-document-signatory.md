# Update Document Signatory with fynk

Updates a document signatory in fynk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document/signatories/:signatory`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Update Document Signatory](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | yes | Document UUID. |
| `mobile_phone` | body | `string` | no | The signatory mobile phone number in E.164 format. |
| `signatory` | path | `string` | yes | Signatory UUID. |
