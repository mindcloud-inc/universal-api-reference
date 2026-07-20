# Shuffle Pile with Deck of Cards

Shuffles a pile in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/pile/{{pile_name}}/shuffle/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Shuffle Pile](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `pile_name` | path | `string` | yes | Pile name to shuffle. |
