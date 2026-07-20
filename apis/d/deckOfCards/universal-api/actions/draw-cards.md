# Deck of Cards: Draw Cards

Draws cards from a deck in Deck of Cards.

```
PUT https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/draw-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/draw-cards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deck_id": "new"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/draw-cards', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deck_id": "new"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deck_id` | string | yes | Deck identifier returned by a create deck action, or new to create a shuffled deck and draw immediately. Default: `new`. |
| `count` | number | no | Number of cards to draw. Default: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": [
        {}
      ],
      "deck_id": "string",
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
| `cards` | array<object> | Cards drawn from the deck. |
| `deck_id` | string | Identifier for the deck. |
| `remaining` | number | Cards remaining in the deck. |
| `success` | boolean | Whether the draw operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/{{deck_id}}/draw/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/draw-cards.md) for the provider-specific parameters and requirements.

