# Deck of Cards: Add Cards to Pile

Adds cards to a pile in Deck of Cards.

```
PUT https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/add-cards-to-pile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/add-cards-to-pile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deck_id": "string",
  "pile_name": "discard",
  "cards": "AS,2S"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/add-cards-to-pile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deck_id": "string",
    "pile_name": "discard",
    "cards": "AS,2S"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deck_id` | string | yes | Deck identifier returned by a create deck action. |
| `pile_name` | string | yes | Pile name to create or update, such as discard or player1. Default: `discard`. |
| `cards` | string | yes | Comma-separated card codes to add to the pile, such as AS,2S. Default: `AS,2S`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deck_id": "string",
      "piles": {},
      "remaining": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deck_id` | string | Identifier for the deck. |
| `piles` | object | Pile state keyed by pile name. |
| `remaining` | number | Cards remaining in the main deck. |
| `success` | boolean | Whether the pile operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/{{deck_id}}/pile/{{pile_name}}/add/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-cards-to-pile.md) for the provider-specific parameters and requirements.

