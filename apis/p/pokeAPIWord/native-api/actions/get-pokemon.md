# Get Pokemon with PokeAPI Word

Retrieves details for a Pokemon from PokeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `pokemon/[:pokemonId]`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokemon](https://pokeapi.co/docs/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pokemonId` | path | `string` | yes | Identifier for the requested Pokemon record. Use an ID or name, such as 1 or bulbasaur. |
