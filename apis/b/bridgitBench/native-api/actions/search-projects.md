# Search Projects with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Projects/_filter`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Search Projects](https://developers.gobridgit.com/reference/projects_queryfilter)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `predicates` | body | `object` | no | — |
| `predicates.projectIds[]` | body | `array<number>` | no | — |
| `predicates.projectState` | body | `list<string>` | yes | Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
| `predicates.name` | body | `string` | no | — |
| `predicates.issues` | body | `list<number>` | yes | Accepted values: `0`, `1`, `2`. |
| `predicates.relativeDate` | body | `date` | yes | — |
| `predicates.includeProjectNumber` | body | `boolean` | yes | — |
