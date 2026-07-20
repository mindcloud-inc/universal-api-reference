# Query Rocks with Ninety.io

Retrieves rocks from Ninety.io with optional filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/rocks/query`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Query Rocks](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortField` | body | `string` | yes | — |
| `sortDirection` | body | `string` | yes | — |
| `pageSize` | body | `number` | yes | — |
| `pageIndex` | body | `number` | yes | — |
| `teamId` | body | `string` | no | Filter Rocks by team Id |
| `userId` | body | `string` | no | Filter Rocks by owner user Id |
| `statusCode` | body | `string` | no | Filter Rocks by status |
| `levelCode` | body | `string` | no | Filter Rocks by level |
| `futureScope` | body | `string` | no | Filter by future scope |
| `archived` | body | `boolean` | no | True for archived Rocks only, false for active Rocks only |
| `searchText` | body | `string` | no | Filter Rocks by title or description text |
| `includeRockGoals` | body | `boolean` | no | When true, linked goals are included in the response |
| `userIds` | body | `string` | no | Comma-separated list of user Ids to filter Rocks by |
