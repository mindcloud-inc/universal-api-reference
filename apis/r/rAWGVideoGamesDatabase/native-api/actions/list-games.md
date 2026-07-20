# List Games with RAWG Video Games Database

Retrieves games from RAWG Video Games Database.

## Endpoint

- **Method:** `GET`
- **Path:** `/games`
- **Base URL:** `https://api.rawg.io/api`
- **Official documentation:** [List Games](https://api.rawg.io/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search query. |
| `search_precise` | query | `boolean` | no | Disable fuzziness for the search query. |
| `search_exact` | query | `boolean` | no | Mark the search query as exact. |
| `ordering` | query | `string` | no | Sort games by name, released, added, created, updated, rating, or metacritic. Prefix with - for descending. |
