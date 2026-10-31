# Reactivate Person with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/:id/restore`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Reactivate Person](https://developers.gobridgit.com/reference/persons_restore)

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
| `rehireDate` | body | `date` | no | The date the new stint starts. Left empty, the person is reactivated with no hire date. |
