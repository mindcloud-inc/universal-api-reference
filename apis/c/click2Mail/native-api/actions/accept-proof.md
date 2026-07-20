# Accept Proof with Click2Mail

Accepts a proof for a Click2Mail job.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/jobs/{id}/proof/accept`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Accept Proof](https://developers.click2mail.com/reference/acceptproof)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | job id |
| `acceptId` | query | `string` | yes | acceptId |
