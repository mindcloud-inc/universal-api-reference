# Download Sign Request Document with Stiply

Downloads a Stiply sign request document as a PDF.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/documents/:document/actions/download_file`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Download Sign Request Document](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadDocumentFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
| `document` | path | `number` | yes | Id of the document. |
