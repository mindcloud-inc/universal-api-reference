# Get Proof with Click2Mail

Retrieves a proof file from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/jobs/{id}/proof/{proofId}/{sessionId}`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Get Proof](https://developers.click2mail.com/reference/getproof)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | job id |
| `proofId` | path | `number` | yes | proof id |
| `sessionId` | path | `string` | yes | — |
