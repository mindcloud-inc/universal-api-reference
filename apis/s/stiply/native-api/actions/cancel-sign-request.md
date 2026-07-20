# Cancel Sign Request with Stiply

Cancels an existing Stiply sign request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sign_requests/:sign_request/actions/cancel`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Cancel Sign Request](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/CancelSignRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
| `notify_signers` | body | `boolean` | yes | Provide whether the signers needs to be informed about the cancelation of the sign request. |
| `cancellation_message` | body | `string` | no | Optional message to show the signers. |
