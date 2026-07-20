# List Pile Cards with Deck of Cards

Retrieves cards in a pile from Deck of Cards.

## Endpoint

- **Method:** `GET`
- **Path:** `deck/{{deck_id}}/pile/{{pile_name}}/list/`
- **Base URL:** `https://www.deckofcardsapi.com/api/`
- **Official documentation:** [List Pile Cards](https://www.deckofcardsapi.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deck_id` | path | `string` | yes | Deck identifier returned by a create deck action. |
| `pile_name` | path | `string` | yes | Pile name to list. |
