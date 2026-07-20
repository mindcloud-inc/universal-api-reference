# Query To-Dos with Ninety.io

Retrieves to-dos from Ninety.io with optional filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/todos/query`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Query To-Dos](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `string` | no | Filter results to a specific team Id |
| `sort` | body | `string` | no | The field to sort results by |
| `order` | body | `string` | no | Sort direction |
| `page` | body | `number` | no | Page number (1-based) |
| `pageSize` | body | `number` | no | Number of results per page |
| `isPersonal` | body | `boolean` | no | Filter to personal To-Dos only |
| `completed` | body | `boolean` | no | Filter by completed status |
| `archived` | body | `boolean` | no | Filter by archived status |
| `searchText` | body | `string` | no | Search text to match against To-Do title and description |
| `title` | body | `string` | no | Filter by exact title match |
