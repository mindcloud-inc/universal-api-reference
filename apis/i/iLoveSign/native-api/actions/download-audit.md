# Download Audit with iLoveSign

## Endpoint

- **Method:** `GET`
- **Path:** `https://:server/v1/signature/:token_requester/download-audit`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Download Audit](https://www.iloveapi.com/docs/api-reference#download-audit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Task-assigned host returned by the start/sign call. |
| `token_requester` | path | `string` | yes | Signature request token requester identifier. |
