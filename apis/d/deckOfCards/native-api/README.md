# Deck of Cards: Native API Reference

A consolidated summary of Deck of Cards's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.deckofcardsapi.com/
- **API base URL:** `https://www.deckofcardsapi.com/api/`

## Authentication

### No Authentication

The Deck of Cards API is public and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.deckofcardsapi.com/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cards to Pile](actions/add-cards-to-pile.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/add/` | [docs](https://www.deckofcardsapi.com/) |
| [Create New Deck](actions/create-new-deck.md) | `GET deck/new/` | [docs](https://www.deckofcardsapi.com/) |
| [Create Shuffled Deck](actions/create-shuffled-deck.md) | `GET deck/new/shuffle/` | [docs](https://www.deckofcardsapi.com/) |
| [Draw Cards](actions/draw-cards.md) | `GET deck/{{deck_id}}/draw/` | [docs](https://www.deckofcardsapi.com/) |
| [Draw Cards from Bottom of Pile](actions/draw-cards-from-bottom-of-pile.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/draw/bottom/` | [docs](https://www.deckofcardsapi.com/) |
| [Draw Cards from Pile](actions/draw-cards-from-pile.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/draw/` | [docs](https://www.deckofcardsapi.com/) |
| [Draw Random Cards from Pile](actions/draw-random-cards-from-pile.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/draw/random/` | [docs](https://www.deckofcardsapi.com/) |
| [List Pile Cards](actions/list-pile-cards.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/list/` | [docs](https://www.deckofcardsapi.com/) |
| [Reshuffle Deck](actions/reshuffle-deck.md) | `GET deck/{{deck_id}}/shuffle/` | [docs](https://www.deckofcardsapi.com/) |
| [Return Cards to Deck](actions/return-cards-to-deck.md) | `GET deck/{{deck_id}}/return/` | [docs](https://www.deckofcardsapi.com/) |
| [Return Pile Cards to Deck](actions/return-pile-cards-to-deck.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/return/` | [docs](https://www.deckofcardsapi.com/) |
| [Shuffle Pile](actions/shuffle-pile.md) | `GET deck/{{deck_id}}/pile/{{pile_name}}/shuffle/` | [docs](https://www.deckofcardsapi.com/) |
