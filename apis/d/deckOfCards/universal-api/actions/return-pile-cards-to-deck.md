# Deck of Cards: Return Pile Cards to Deck

Returns pile cards to a deck in Deck of Cards.

```
PUT https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/return-pile-cards-to-deck
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/return-pile-cards-to-deck" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deck_id": "string",
  "pile_name": "discard"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/return-pile-cards-to-deck', {
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
| `pile_name` | string | yes | Pile name whose cards should be returned to the main deck. Default: `discard`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cards` | string | no | Optional comma-separated card codes to return from the pile to the main deck. |

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
| `success` | boolean | Whether the pile return operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/{{deck_id}}/pile/{{pile_name}}/return/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/return-pile-cards-to-deck.md) for the provider-specific parameters and requirements.

