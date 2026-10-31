# Update Person with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person](https://developers.gobridgit.com/reference/persons_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Person ID |
| `payload` | body | `object` | yes | — |
