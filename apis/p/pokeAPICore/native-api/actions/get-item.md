# Get Item with PokeAPI Core

Retrieves an item from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Item](https://pokeapi.co/docs/v2#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Item numeric ID or exact PokeAPI item name. |
