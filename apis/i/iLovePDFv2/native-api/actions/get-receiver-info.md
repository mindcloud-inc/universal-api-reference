# Get Receiver Info with iLovePDFv2

Retrieves a signature receiver from iLovePDFv2 by receiver token.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature/receiver/info/:receiver_token_requester`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Get Receiver Info](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receiver_token_requester` | path | `string` | yes | Receiver token requester value. |
