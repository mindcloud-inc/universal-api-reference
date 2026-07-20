# Scryfall: Native API Reference

A consolidated summary of Scryfall's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://scryfall.com/docs/api
- **API base URL:** `https://api.scryfall.com/`

## Authentication

### None

This API does not require request authentication.

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud/1.0 (apps@mindcloud.co)` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Card Names](actions/autocomplete-card-names.md) | `GET cards/autocomplete` | [docs](https://scryfall.com/docs/api/cards) |
| [Get Bulk Data](actions/get-bulk-data.md) | `GET bulk-data/:type` | [docs](https://scryfall.com/docs/api/bulk-data) |
| [Get Card By Arena ID](actions/get-card-by-arena-id.md) | `GET cards/arena/:id` | [docs](https://scryfall.com/docs/api/cards) |
| [Get Card By MTGO ID](actions/get-card-by-mtgo-id.md) | `GET cards/mtgo/:id` | [docs](https://scryfall.com/docs/api/cards) |
| [Get Card By Multiverse ID](actions/get-card-by-multiverse-id.md) | `GET cards/multiverse/:id` | [docs](https://scryfall.com/docs/api/cards) |
| [Get Card By Name](actions/get-card-by-name.md) | `GET cards/named` | [docs](https://scryfall.com/docs/api/cards/named) |
| [Get Card By Scryfall ID](actions/get-card-by-scryfall-id.md) | `GET cards/:id` | [docs](https://scryfall.com/docs/api/cards) |
| [Get Card By Set And Number](actions/get-card-by-set-and-number.md) | `GET cards/:code/:number` | [docs](https://scryfall.com/docs/api/cards) |
| [Get Card Rulings](actions/get-card-rulings.md) | `GET cards/:id/rulings` | [docs](https://scryfall.com/docs/api/rulings) |
| [Get MTGO Card Rulings](actions/get-mtgo-card-rulings.md) | `GET cards/mtgo/:id/rulings` | [docs](https://scryfall.com/docs/api/rulings) |
| [Get Multiverse Card Rulings](actions/get-multiverse-card-rulings.md) | `GET cards/multiverse/:id/rulings` | [docs](https://scryfall.com/docs/api/rulings) |
| [Get Random Card](actions/get-random-card.md) | `GET cards/random` | [docs](https://scryfall.com/docs/api/cards/random) |
| [Get Set](actions/get-set.md) | `GET sets/:code` | [docs](https://scryfall.com/docs/api/sets/code) |
| [List Artifact Types](actions/list-artifact-types.md) | `GET catalog/artifact-types` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Artist Names](actions/list-artist-names.md) | `GET catalog/artist-names` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Bulk Data](actions/list-bulk-data.md) | `GET bulk-data` | [docs](https://scryfall.com/docs/api/bulk-data) |
| [List Card Names](actions/list-card-names.md) | `GET catalog/card-names` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Card Symbols](actions/list-card-symbols.md) | `GET symbology` | [docs](https://scryfall.com/docs/api/card-symbols) |
| [List Creature Types](actions/list-creature-types.md) | `GET catalog/creature-types` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Enchantment Types](actions/list-enchantment-types.md) | `GET catalog/enchantment-types` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Keyword Abilities](actions/list-keyword-abilities.md) | `GET catalog/keyword-abilities` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Land Types](actions/list-land-types.md) | `GET catalog/land-types` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Planeswalker Types](actions/list-planeswalker-types.md) | `GET catalog/planeswalker-types` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Powers](actions/list-powers.md) | `GET catalog/powers` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Sets](actions/list-sets.md) | `GET sets` | [docs](https://scryfall.com/docs/api/sets/all) |
| [List Spell Types](actions/list-spell-types.md) | `GET catalog/spell-types` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Toughnesses](actions/list-toughnesses.md) | `GET catalog/toughnesses` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Watermarks](actions/list-watermarks.md) | `GET catalog/watermarks` | [docs](https://scryfall.com/docs/api/catalogs) |
| [List Word Bank](actions/list-word-bank.md) | `GET catalog/word-bank` | [docs](https://scryfall.com/docs/api/catalogs) |
| [Search Cards](actions/search-cards.md) | `GET cards/search` | [docs](https://scryfall.com/docs/api/cards/search) |
