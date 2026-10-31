# Search People with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/_filter`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Search People](https://developers.gobridgit.com/reference/persons_queryfilter)

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
| `predicates.personIds[]` | body | `array<number>` | no | — |
| `predicates.state` | body | `list<string>` | yes | Accepted values: `Active`, `All`, `Deactivated`. |
| `predicates.email` | body | `string` | no | — |
| `predicates.uniqueId` | body | `string` | no | — |
| `predicates.relativeDate` | body | `date` | yes | — |
