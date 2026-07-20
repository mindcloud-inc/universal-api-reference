# Return Cards to Deck with Deck of Cards

Returns cards to a deck in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/return/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Return Cards to Deck](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `cards` | query | `string` | no | Optional comma-separated card codes to return to the main deck. |
