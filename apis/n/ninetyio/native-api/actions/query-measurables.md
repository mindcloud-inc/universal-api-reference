# Query Measurables with Ninety.io

Retrieves measurables from Ninety.io with optional filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scorecard/kpis/query`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Query Measurables](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `excludeKpiIds[]` | body | `array<string>` | no | Array of Measurable Ids to exclude from the response |
| `pageIndex` | body | `number` | no | The page number to retrieve |
| `pageSize` | body | `number` | no | The number of items to retrieve per page |
| `periodInterval` | body | `string` | no | Limits results to Measurables with the specified period interval |
| `searchOwner` | body | `string` | no | The name of the owner of the Measurables to retrieve |
| `searchText` | body | `string` | no | Text to search for in the Measurable title or description |
| `searchTitle` | body | `string` | no | Text to search for in the Measurable title only |
| `sortField` | body | `string` | no | The field to sort Measurables by |
| `sortDirection` | body | `string` | no | The sort direction for the selected sort field |
| `unassignedOnly` | body | `boolean` | no | Only include Measurables that have no owner assigned |
| `userIds[]` | body | `array<string>` | no | An array of user Ids to filter Measurables by owner |
