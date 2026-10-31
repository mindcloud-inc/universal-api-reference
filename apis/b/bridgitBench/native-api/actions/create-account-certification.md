# Create Account Certification with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/certifications`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Account Certification](https://developers.gobridgit.com/reference/accountcertifications_add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `name` | body | `string` | yes | — |
| `abbreviation` | body | `string` | yes | — |
| `requireExpiration` | body | `boolean` | yes | — |
| `daysWarnBeforeExpire` | body | `number` | no | — |
