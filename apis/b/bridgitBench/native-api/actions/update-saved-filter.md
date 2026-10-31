# Update Saved Filter with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/my-filters/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Saved Filter](https://developers.gobridgit.com/reference/userfilters_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the filter to remove |
| `name` | body | `string` | no | — |
| `filtersSet[]` | body | `array<object>` | no | — |
| `filtersSet[].type` | body | `list<string>` | yes | Accepted values: `People`, `Project`, `Roles`. |
| `filtersSet[].fieldDefId` | body | `number` | no | — |
| `filtersSet[].filterType` | body | `string` | yes | — |
| `filtersSet[].filters[]` | body | `array<object>` | yes | — |
| `filtersSet[].filters[].verb` | body | `list<string>` | no | Accepted values: `Above`, `Below`, `Between`, `Equals`, `Excludes`, `Includes`. |
| `filtersSet[].filters[].valueIds[]` | body | `array<number>` | no | — |
| `filtersSet[].filters[].shortValues[]` | body | `array<number>` | no | — |
| `filtersSet[].filters[].intValues[]` | body | `array<number>` | no | — |
| `filtersSet[].filters[].longValues[]` | body | `array<number>` | no | — |
| `filtersSet[].filters[].decimalValues[]` | body | `array<number>` | no | — |
| `filtersSet[].filters[].dateValues[]` | body | `array<date>` | no | — |
| `filtersSet[].filters[].stringValue` | body | `string` | no | — |
| `filtersSet[].filters[].blankValue` | body | `boolean` | no | — |
| `filtersSet[].filters[].dynamicData` | body | `object` | no | — |
