# Download Signed PDF with Mifiel

Retrieves a signed document PDF from Mifiel.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/documents/:id/file_signed`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Download Signed PDF](https://docs.mifiel.com/en/#tag/Get-signed-document/operation/GetSignedDocumentPDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Document ID. |
