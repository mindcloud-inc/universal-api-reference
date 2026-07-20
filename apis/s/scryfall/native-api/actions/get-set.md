# Get Set with Scryfall

Retrieves a card set from Scryfall by code.

## Endpoint

- **Method:** `GET`
- **Path:** `sets/:code`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Get Set](https://scryfall.com/docs/api/sets/code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Three to five-letter Scryfall or MTGO set code. |
