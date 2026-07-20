# Search Cards with Vistaly

Finds cards in Vistaly by semantic search.

## Endpoint

- **Method:** `POST`
- **Path:** `/beta/cards/search`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Search Cards](https://docs.vistaly.com/api-reference/cards/search-cards-using-semantic-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Natural language search query that finds cards with similar content. |
| `filter` | body | `object` | no | Optional filter object with must, must_not, and should clauses for card metadata. |
