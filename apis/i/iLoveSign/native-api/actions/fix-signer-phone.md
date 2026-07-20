# Fix Signer Phone with iLoveSign

## Endpoint

- **Method:** `PUT`
- **Path:** `/signature/signer/fix-phone/:signer_token_requester`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Fix Signer Phone](https://www.iloveapi.com/docs/api-reference#fix-signer-phone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signer_token_requester` | path | `string` | yes | Signer token requester identifier. |
| `phone` | body | `string` | yes | Replacement mobile number including country prefix digits only. |
