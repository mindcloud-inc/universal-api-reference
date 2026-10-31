# List Hourly Role Names with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:id/hourly-role-names`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Hourly Role Names](https://developers.gobridgit.com/reference/hourlyrolenames_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The account ID |
| `excludeArchived` | query | `boolean` | no | Optional flag to leave archived hourly role names out of the response. All hourly role names are returned when omitted |
