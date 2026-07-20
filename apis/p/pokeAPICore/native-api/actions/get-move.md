# Get Move with PokeAPI Core

Retrieves a move from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/move/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Move](https://pokeapi.co/docs/v2#moves)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Move numeric ID or exact PokeAPI move name. |
