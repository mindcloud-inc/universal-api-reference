# Draw Random Cards from Pile with Deck of Cards

Draws random cards from a pile in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/pile/{{pile_name}}/draw/random/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Draw Random Cards from Pile](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `pile_name` | path | `string` | yes | Pile name to draw from. |
| `count` | query | `number` | no | Number of random cards to draw from the pile. |
