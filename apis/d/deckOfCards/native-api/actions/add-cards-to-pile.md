# Add Cards to Pile with Deck of Cards

Adds cards to a pile in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/pile/{{pile_name}}/add/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Add Cards to Pile](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `pile_name` | path | `string` | yes | Pile name to create or update, such as discard or player1. |
| `cards` | query | `string` | yes | Comma-separated card codes to add to the pile, such as AS,2S. |
