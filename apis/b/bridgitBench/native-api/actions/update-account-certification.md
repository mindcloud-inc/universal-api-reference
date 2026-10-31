# Update Account Certification with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/certifications/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Account Certification](https://developers.gobridgit.com/reference/accountcertifications_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the certification to update |
| `payload` | body | `object` | yes | — |
