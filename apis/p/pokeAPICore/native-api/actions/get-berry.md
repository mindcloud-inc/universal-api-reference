# Get Berry with PokeAPI Core

Retrieves a berry from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/berry/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Berry](https://pokeapi.co/docs/v2#berries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Berry numeric ID or exact PokeAPI berry name. |
