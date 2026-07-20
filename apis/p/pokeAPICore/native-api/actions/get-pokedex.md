# Get Pokedex with PokeAPI Core

Retrieves a Pokedex from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/pokedex/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokedex](https://pokeapi.co/docs/v2#pokedexes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Pokedex numeric ID or exact PokeAPI pokedex name. |
