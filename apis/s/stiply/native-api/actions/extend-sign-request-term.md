# Extend Sign Request Term with Stiply

Extends the term of a Stiply sign request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sign_requests/:sign_request/actions/extend_term`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Extend Sign Request Term](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/ExtendSignRequestTerm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
| `term` | body | `string` | yes | 2 digit code representing the sign term (1d = one day, 2w = two weeks, 3m = three months). When omitted, the account's configured default term will be used. |
| `notify_signers` | body | `boolean` | no | Provide whether the signers needs to be informed about the extension of the term of the sign request. |
