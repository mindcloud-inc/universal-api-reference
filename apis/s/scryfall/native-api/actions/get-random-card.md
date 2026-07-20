# Get Random Card with Scryfall

Retrieves a random card from Scryfall.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/random`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Random Card](https://scryfall.com/docs/api/cards/random)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional Scryfall query used to filter the random card pool. |
