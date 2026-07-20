# Deck of Cards: Draw Random Cards from Pile

Draws random cards from a pile in Deck of Cards.

```
PUT https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/draw-random-cards-from-pile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/draw-random-cards-from-pile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deck_id": "string",
  "pile_name": "discard"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/draw-random-cards-from-pile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deck_id": "string",
    "pile_name": "discard"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deck_id` | string | yes | Deck identifier returned by a create deck action. |
| `pile_name` | string | yes | Pile name to draw from. Default: `discard`. |
| `count` | number | no | Number of random cards to draw from the pile. Default: `1`. |

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
      "piles": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | array<object> | Random cards drawn from the pile. |
| `deck_id` | string | Identifier for the deck. |
| `piles` | object | Pile state keyed by pile name. |
| `success` | boolean | Whether the pile draw operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/{{deck_id}}/pile/{{pile_name}}/draw/random/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/draw-random-cards-from-pile.md) for the provider-specific parameters and requirements.

