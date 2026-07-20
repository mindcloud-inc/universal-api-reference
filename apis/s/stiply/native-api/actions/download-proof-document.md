# Download Proof Document with Stiply

Downloads the proof document for a completed Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/actions/download_proof_document`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Download Proof Document](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadProofDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
