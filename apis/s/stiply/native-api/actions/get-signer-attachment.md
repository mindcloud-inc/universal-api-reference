# Get Signer Attachment with Stiply

Retrieves a signer attachment from a Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/signer_attachments/:signer_attachment`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Get Signer Attachment](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSignerAttachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
| `signer_attachment` | path | `number` | yes | Id of the signer attachment. |
