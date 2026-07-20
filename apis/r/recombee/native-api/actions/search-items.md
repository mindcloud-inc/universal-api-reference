# Search Items with Recombee

Searches items for a user in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/users/:userId/items/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Search Items](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `count` | body | `string` | no |
| `searchQuery` | body | `string` | yes |
| `userId` | path | `string` | yes |
