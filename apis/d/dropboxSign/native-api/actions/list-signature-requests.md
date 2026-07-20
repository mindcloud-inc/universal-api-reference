# List Signature Requests with Dropbox Sign

Retrieves signature requests from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_request/list`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [List Signature Requests](https://developers.hellosign.com/api/reference/operation/signatureRequestList/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | query | `string` | no | Which account to return SignatureRequests for. Use all for all team members. |
| `query` | query | `string` | no | Search terms used to filter signature requests. |
