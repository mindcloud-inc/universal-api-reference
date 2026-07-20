# Create Shuffled Deck with Deck of Cards

Creates a shuffled deck in Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/new/shuffle/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [Create Shuffled Deck](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_count` | query | `number` | no | Number of standard decks to include. Defaults to 1. |
| `cards` | query | `string` | no | Optional comma-separated card codes for a partial deck, such as AS,2S,KS. |
