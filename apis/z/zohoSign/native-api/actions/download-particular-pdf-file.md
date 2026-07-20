# Download Particular PDF File with Zoho Sign

Downloads a particular PDF file from Zoho Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/:requestId/documents/:documentId/pdf`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Download Particular PDF File](https://www.zoho.com/sign/api/document-managment/download-particular-pdf.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Zoho Sign request identifier. |
| `documentId` | path | `string` | yes | Zoho Sign document identifier inside the request. |
