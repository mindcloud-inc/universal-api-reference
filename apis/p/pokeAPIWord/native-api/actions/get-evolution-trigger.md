# Get Evolution Trigger with PokeAPI Word

Retrieves evolution trigger details from PokeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `evolution-trigger/[:evolutionTriggerId]`
- **Base URL:** `https://pokeapi.co/api/v2`
- **Official documentation:** [Get Evolution Trigger](https://pokeapi.co/docs/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evolutionTriggerId` | path | `string` | yes | Identifier for the requested evolution trigger. Use an ID or name. |
