# Search Account Activities with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/activities/_filter`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Search Account Activities](https://developers.gobridgit.com/reference/accountactivities_filter)

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
| `accountId` | path | `number` | yes | The account ID (must be greater than zero) |
| `predicates` | body | `object` | no | — |
| `predicates.personIds[]` | body | `array<number>` | yes | — |
| `predicates.projectIds[]` | body | `array<number>` | yes | — |
| `predicates.happenedFrom` | body | `date` | no | — |
| `predicates.happenedTo` | body | `date` | no | — |
| `predicates.triggeredByUserIds[]` | body | `array<number>` | yes | — |
| `predicates.activityTypes[]` | body | `array<string>` | yes | — |
| `predicates.triggeredByIntegrations` | body | `boolean` | yes | — |
| `predicates.triggeredByUsers` | body | `boolean` | yes | — |
| `predicates.groupingIds[]` | body | `array<number>` | yes | — |
| `predicates.includeBlankGroupIds` | body | `boolean` | yes | — |
| `predicates.activityTypeSearch` | body | `string` | yes | Maximum length: 100. |
