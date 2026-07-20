# List Sign Request Progress with Stiply

Retrieves progress entries for a Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/progress`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [List Sign Request Progress](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestProgress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
