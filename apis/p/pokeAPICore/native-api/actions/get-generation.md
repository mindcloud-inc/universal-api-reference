# Get Generation with PokeAPI Core

Retrieves a generation from PokeAPI Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/generation/[:idOrName]/`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Generation](https://pokeapi.co/docs/v2#generations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | Generation numeric ID or exact PokeAPI generation name. |
