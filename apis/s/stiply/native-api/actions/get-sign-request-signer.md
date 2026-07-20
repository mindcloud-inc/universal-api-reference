# Get Sign Request Signer with Stiply

Retrieves a signer from a Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/signers/:signer`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Get Sign Request Signer](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSigner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
| `signer` | path | `number` | yes | Id of the signer. |
