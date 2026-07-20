# Download Signer Attachments with Stiply

Downloads all attachments uploaded by a Stiply signer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/signers/:signer/actions/download_signer_attachments`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Download Signer Attachments](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadSignerAttachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
| `signer` | path | `number` | yes | Id of the signer. |
