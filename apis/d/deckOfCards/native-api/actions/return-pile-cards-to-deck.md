# Return Pile Cards to Deck with Deck of Cards

Returns pile cards to a deck in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/pile/{{pile_name}}/return/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Return Pile Cards to Deck](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `pile_name` | path | `string` | yes | Pile name whose cards should be returned to the main deck. |
| `cards` | query | `string` | no | Optional comma-separated card codes to return from the pile to the main deck. |
