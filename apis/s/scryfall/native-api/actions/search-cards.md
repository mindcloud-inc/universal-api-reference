# Search Cards with Scryfall

Finds cards in Scryfall by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `cards/search`
- **Base URL:** `https://api.scryfall.com/`
- **Official documentation:** [Search Cards](https://scryfall.com/docs/api/cards/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Scryfall full-text search query. |
| `unique` | query | `string` | no | How duplicate prints should be collapsed, such as cards, art, or prints. |
| `order` | query | `string` | no | Sort order for matching cards, such as name, set, released, rarity, usd, eur, cmc, power, toughness, or edhrec. |
| `dir` | query | `string` | no | Sort direction, auto, asc, or desc. |
| `include_extras` | query | `boolean` | no | Include extra cards such as tokens, planes, schemes, and funny cards. |
| `page` | query | `number` | no | Result page number for paginated card search. |
