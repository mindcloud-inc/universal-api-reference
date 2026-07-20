# List Signatures with iLovePDFv2

Lists signature requests in iLovePDFv2.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature/list`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [List Signatures](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Signature page, starting at 0. |
| `per-page` | query | `number` | no | Number of signatures to return, from 1 to 100. |
