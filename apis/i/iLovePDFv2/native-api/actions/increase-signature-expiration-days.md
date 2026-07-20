# Increase Signature Expiration Days with iLovePDFv2

## Endpoint

- **Method:** `POST`
- **Path:** `/signature/increase-expiration-days/:token_requester`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Increase Signature Expiration Days](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token_requester` | path | `string` | yes | Signature requester token. |
| `days` | body | `number` | yes | Days to add, between 1 and 130. |
