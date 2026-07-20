# Get Pokemon with PokeAPI Core

Retrieves a Pokemon from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/pokemon/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokemon](https://pokeapi.co/docs/v2#pokemon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Pokemon numeric ID or exact PokeAPI name, such as ditto. |
