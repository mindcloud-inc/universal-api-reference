# Create Saved Filter with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/my-filters`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Saved Filter](https://developers.gobridgit.com/reference/userfilters_add)

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
| `type` | body | `list<string>` | yes | Accepted values: `People`, `Project`, `Roles`. |
| `filtersSet[]` | body | `array<object>` | yes | — |
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
