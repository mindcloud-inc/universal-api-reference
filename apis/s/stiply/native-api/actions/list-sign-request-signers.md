# List Sign Request Signers with Stiply

Retrieves signers for a Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/signers`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [List Sign Request Signers](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSigners)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
