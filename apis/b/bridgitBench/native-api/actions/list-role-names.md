# List Role Names with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/role-names`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Role Names](https://developers.gobridgit.com/reference/rolenames_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `excludeArchived` | query | `boolean` | no | Optional flag to leave archived role names out of the response. All role names are returned when omitted |
