# Search Person Collaborations with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/Accounts/:id/collaboration-matrix/_filter`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Search Person Collaborations](https://developers.gobridgit.com/reference/accounts_querycollaborationmatrix)

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
| `id` | path | `number` | yes | The account ID |
| `predicates` | body | `object` | no | — |
| `predicates.personIds[]` | body | `array<number>` | no | — |
| `predicates.projectId` | body | `number` | no | — |
| `predicates.roleType` | body | `list<string>` | yes | Accepted values: `All`, `Hourly`, `Salaried`. |
| `predicates.salariedRoleType` | body | `list<string>` | yes | Accepted values: `All`, `Operations`, `Preconstruction`. |
| `predicates.roleNameIds[]` | body | `array<number>` | no | — |
