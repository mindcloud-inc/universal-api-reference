# Get Pokemon Species with PokeAPI Core

Retrieves a Pokemon species from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/pokemon-species/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Pokemon Species](https://pokeapi.co/docs/v2#pokemon-species)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Pokemon species numeric ID or exact PokeAPI species name. |
