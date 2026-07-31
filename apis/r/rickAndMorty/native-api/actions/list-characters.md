# List Characters with Rick and Morty

## Endpoint

- **Method:** `GET`
- **Path:** `/character`
- **Base URL:** `https://rickandmortyapi.com/api`
- **Official documentation:** [List Characters](https://rickandmortyapi.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page of results. |
| `name` | query | `string` | no | Filter by name. |
| `status` | query | `string` | no | Filter by alive, dead, or unknown. |
| `species` | query | `string` | no | Filter by species. |
| `type` | query | `string` | no | Filter by type. |
| `gender` | query | `string` | no | Filter by female, male, genderless, or unknown. |
