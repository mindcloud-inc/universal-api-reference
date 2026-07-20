# Get Signature Request Status with DigiSigner

Retrieves a DigiSigner signature request by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_requests/:signatureRequestId`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Get Signature Request Status](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | DigiSigner signature_request_id returned by Send Signature Request. |
