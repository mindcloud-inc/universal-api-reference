# <img src="https://images.mindcloud.co/apps/icons/deck-of-cards_1777482391340.png" alt="Deck of Cards logo" width="28" height="28"> Deck of Cards: Universal API

Use the public Deck of Cards API to create, shuffle, draw from, and manage card decks and piles.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deckOfCards/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deckofcardsapi.com/
- **Vendor API docs:** https://www.deckofcardsapi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pile Cards](actions/list-pile-cards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/list-pile-cards?connectionId=$CONNECTION_ID&deck_id=string&pile_name=discard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Card Draw

| Action | Method | Description |
| --- | --- | --- |
| [Draw Cards](actions/draw-cards.md) | PUT | Draws cards from a deck in Deck of Cards. |

### Deck

| Action | Method | Description |
| --- | --- | --- |
| [Create New Deck](actions/create-new-deck.md) | POST | Creates a new deck in Deck of Cards. |
| [Create Shuffled Deck](actions/create-shuffled-deck.md) | POST | Creates a shuffled deck in Deck of Cards. |
| [Reshuffle Deck](actions/reshuffle-deck.md) | PUT | Reshuffles a deck in Deck of Cards. |
| [Return Cards to Deck](actions/return-cards-to-deck.md) | PUT | Returns cards to a deck in Deck of Cards. |

### Pile

| Action | Method | Description |
| --- | --- | --- |
| [Add Cards to Pile](actions/add-cards-to-pile.md) | PUT | Adds cards to a pile in Deck of Cards. |
| [List Pile Cards](actions/list-pile-cards.md) | GET | Retrieves cards in a pile from Deck of Cards. |
| [Return Pile Cards to Deck](actions/return-pile-cards-to-deck.md) | PUT | Returns pile cards to a deck in Deck of Cards. |
| [Shuffle Pile](actions/shuffle-pile.md) | PUT | Shuffles a pile in Deck of Cards. |

### Pile Card Draw

| Action | Method | Description |
| --- | --- | --- |
| [Draw Cards from Bottom of Pile](actions/draw-cards-from-bottom-of-pile.md) | PUT | Draws cards from the bottom of a pile in Deck of Cards. |
| [Draw Cards from Pile](actions/draw-cards-from-pile.md) | PUT | Draws cards from a pile in Deck of Cards. |
| [Draw Random Cards from Pile](actions/draw-random-cards-from-pile.md) | PUT | Draws random cards from a pile in Deck of Cards. |

