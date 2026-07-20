# Autocomplete Card Names with Scryfall

Finds card names in Scryfall by fuzzy text match.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/autocomplete`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Autocomplete Card Names](https://scryfall.com/docs/api/cards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Partial card name for autocomplete suggestions. |
