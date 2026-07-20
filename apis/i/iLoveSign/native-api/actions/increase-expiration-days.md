# Increase Expiration Days with iLoveSign

## Endpoint

- **Method:** `PUT`
- **Path:** `/signature/increase-expiration-days/:token_requester`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Increase Expiration Days](https://www.iloveapi.com/docs/api-reference#signature-increase-expiration-days)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token_requester` | path | `string` | yes | Signature request token requester identifier. |
| `days` | body | `number` | yes | Number of additional days to add, between 1 and 130. |
