# Draw Cards from Bottom of Pile with Deck of Cards

Draws cards from the bottom of a pile in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/pile/{{pile_name}}/draw/bottom/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Draw Cards from Bottom of Pile](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `pile_name` | path | `string` | yes | Pile name to draw from. |
| `count` | query | `number` | no | Number of cards to draw from the bottom of the pile. |
