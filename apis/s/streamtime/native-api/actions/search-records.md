# Search Records with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Search Records](https://api.streamtime.net/v2/swagger#/Search/searchRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_view` | query | `number` | yes | Search view enum that selects which record domain to search. |
| `include_statistics` | query | `boolean` | no | Whether to include the optional statistics object in the response. |
| `wildcardSearch` | body | `string` | no | Free-text search string applied within the selected search view. |
| `offset` | body | `number` | no | Result offset for the search request. |
| `maxResults` | body | `number` | no | Maximum number of results to return. |
| `sortField` | body | `number` | no | Search column enum to sort by. |
| `sortAscending` | body | `boolean` | no | Whether sort order should be ascending. |
| `filterGroupCollection` | body | `object` | yes | Advanced recursive filter DSL object documented by Streamtime for structured searches. |
| `filterGroupCollection.conditionMatchTypeId` | body | `number` | yes | AND/OR enum for the root filter group collection. |
| `filterGroupCollection.filterGroups[]` | body | `array<object>` | yes | Array of filter groups. Streamtime runtime requires this key to be present even for wildcard-only searches. |
