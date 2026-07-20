# List Signer Attachments with Stiply

Retrieves signer attachments for a Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/signer_attachments`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [List Signer Attachments](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSignerAttachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
