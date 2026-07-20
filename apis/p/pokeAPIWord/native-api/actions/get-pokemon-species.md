# Get Pokemon Species with PokeAPI Word

Retrieves Pokemon species details from PokeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `pokemon-species/[:pokemonSpeciesId]`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokemon Species](https://pokeapi.co/docs/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pokemonSpeciesId` | path | `string` | yes | Identifier for the requested Pokemon species. Use an ID or name, such as 1 or bulbasaur. |
