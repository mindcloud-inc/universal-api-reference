# List Sign Request Documents with Stiply

Retrieves documents for a Stiply sign request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/documents`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [List Sign Request Documents](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestDocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
