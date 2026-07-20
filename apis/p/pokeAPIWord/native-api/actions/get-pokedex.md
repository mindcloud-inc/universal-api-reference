# Get Pokedex with PokeAPI Word

Retrieves details for a Pokedex from PokeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `pokedex/[:pokedexId]`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokedex](https://pokeapi.co/docs/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pokedexId` | path | `string` | yes | Identifier for the requested Pokedex. Use an ID or name. |
