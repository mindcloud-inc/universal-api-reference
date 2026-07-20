# Reshuffle Deck with Deck of Cards

Reshuffles a deck in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/shuffle/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Reshuffle Deck](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `remaining` | query | `boolean` | no | When true, shuffle only the remaining cards in the main stack and leave piles or drawn cards alone. |
