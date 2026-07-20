# Get Ability with PokeAPI Core

Retrieves an ability from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/ability/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Ability](https://pokeapi.co/docs/v2#abilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Ability numeric ID or exact PokeAPI ability name. |
