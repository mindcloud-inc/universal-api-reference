# Draw Cards with Deck of Cards

Draws cards from a deck in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/draw/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Draw Cards](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action, or new to create a shuffled deck and draw immediately. |
| `count` | query | `number` | no | Number of cards to draw. |
