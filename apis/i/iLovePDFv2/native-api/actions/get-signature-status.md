# Get Signature Status with iLovePDFv2

Retrieves a signature request from iLovePDFv2 by requester token.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature/requesterview/:token_requester`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Get Signature Status](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token_requester` | path | `string` | yes | Signature requester token. |
