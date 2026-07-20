# Get Pokemon Encounters with PokeAPI Word

Retrieves Pokemon encounter locations from PokeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `pokemon/[:pokemonId]/encounters`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokemon Encounters](https://pokeapi.co/docs/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pokemonId` | path | `string` | yes | Identifier for the Pokemon whose encounter locations should be returned. Use an ID or name. |
