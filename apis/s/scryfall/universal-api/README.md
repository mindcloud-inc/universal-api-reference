# <img src="https://images.mindcloud.co/apps/icons/icon_1746488898626.png" alt="Scryfall logo" width="28" height="28"> Scryfall: Universal API

Scryfall provides a public API for Magic: The Gathering card search, card details, sets, rulings, symbols, catalogs, and bulk data metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scryfall/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scryfall.com
- **Vendor API docs:** https://scryfall.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sets](actions/list-sets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-sets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Artifact Type

| Action | Method | Description |
| --- | --- | --- |
| [List Artifact Types](actions/list-artifact-types.md) | GET | Retrieves the artifact type catalog from Scryfall. |

### Artist Name

| Action | Method | Description |
| --- | --- | --- |
| [List Artist Names](actions/list-artist-names.md) | GET | Retrieves the artist name catalog from Scryfall. |

### Bulk Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Data](actions/get-bulk-data.md) | GET | Retrieves a bulk data record from Scryfall by type. |
| [List Bulk Data](actions/list-bulk-data.md) | GET | Retrieves bulk data records from Scryfall. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Card By Arena ID](actions/get-card-by-arena-id.md) | GET | Retrieves a card from Scryfall by Arena ID. |
| [Get Card By MTGO ID](actions/get-card-by-mtgo-id.md) | GET | Retrieves a card from Scryfall by MTGO ID. |
| [Get Card By Multiverse ID](actions/get-card-by-multiverse-id.md) | GET | Retrieves a card from Scryfall by Multiverse ID. |
| [Get Card By Name](actions/get-card-by-name.md) | GET | Retrieves a card from Scryfall by name. |
| [Get Card By Scryfall ID](actions/get-card-by-scryfall-id.md) | GET | Retrieves a card from Scryfall by Scryfall ID. |
| [Get Card By Set And Number](actions/get-card-by-set-and-number.md) | GET | Retrieves a card from Scryfall by set and collector number. |
| [Get Random Card](actions/get-random-card.md) | GET | Retrieves a random card from Scryfall. |
| [Search Cards](actions/search-cards.md) | GET | Finds cards in Scryfall by search query. |

### Card Name

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Card Names](actions/autocomplete-card-names.md) | GET | Finds card names in Scryfall by fuzzy text match. |
| [List Card Names](actions/list-card-names.md) | GET | Retrieves the card name catalog from Scryfall. |

### Card Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Card Symbols](actions/list-card-symbols.md) | GET | Retrieves card symbols from Scryfall. |

### Creature Type

| Action | Method | Description |
| --- | --- | --- |
| [List Creature Types](actions/list-creature-types.md) | GET | Retrieves the creature type catalog from Scryfall. |

### Enchantment Type

| Action | Method | Description |
| --- | --- | --- |
| [List Enchantment Types](actions/list-enchantment-types.md) | GET | Retrieves the enchantment type catalog from Scryfall. |

### Keyword Ability

| Action | Method | Description |
| --- | --- | --- |
| [List Keyword Abilities](actions/list-keyword-abilities.md) | GET | Retrieves the keyword ability catalog from Scryfall. |

### Land Type

| Action | Method | Description |
| --- | --- | --- |
| [List Land Types](actions/list-land-types.md) | GET | Retrieves the land type catalog from Scryfall. |

### Planeswalker Type

| Action | Method | Description |
| --- | --- | --- |
| [List Planeswalker Types](actions/list-planeswalker-types.md) | GET | Retrieves the planeswalker type catalog from Scryfall. |

### Power

| Action | Method | Description |
| --- | --- | --- |
| [List Powers](actions/list-powers.md) | GET | Retrieves the power value catalog from Scryfall. |

### Ruling

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Rulings](actions/get-card-rulings.md) | GET | Retrieves card rulings from Scryfall by Scryfall ID. |
| [Get MTGO Card Rulings](actions/get-mtgo-card-rulings.md) | GET | Retrieves card rulings from Scryfall by MTGO ID. |
| [Get Multiverse Card Rulings](actions/get-multiverse-card-rulings.md) | GET | Retrieves card rulings from Scryfall by Multiverse ID. |

### Set

| Action | Method | Description |
| --- | --- | --- |
| [Get Set](actions/get-set.md) | GET | Retrieves a card set from Scryfall by code. |
| [List Sets](actions/list-sets.md) | GET | Retrieves all card sets from Scryfall. |

### Spell Type

| Action | Method | Description |
| --- | --- | --- |
| [List Spell Types](actions/list-spell-types.md) | GET | Retrieves the spell type catalog from Scryfall. |

### Toughness

| Action | Method | Description |
| --- | --- | --- |
| [List Toughnesses](actions/list-toughnesses.md) | GET | Retrieves the toughness value catalog from Scryfall. |

### Watermark

| Action | Method | Description |
| --- | --- | --- |
| [List Watermarks](actions/list-watermarks.md) | GET | Retrieves the watermark catalog from Scryfall. |

### Word

| Action | Method | Description |
| --- | --- | --- |
| [List Word Bank](actions/list-word-bank.md) | GET | Retrieves the word bank catalog from Scryfall. |

