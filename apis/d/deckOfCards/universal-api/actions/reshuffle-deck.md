# Deck of Cards: Reshuffle Deck

Reshuffles a deck in Deck of Cards.

```
PUT https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/reshuffle-deck
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/reshuffle-deck" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deck_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/reshuffle-deck', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deck_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deck_id` | string | yes | Deck identifier returned by a create deck action. |
| `remaining` | boolean | no | When true, shuffle only the remaining cards in the main stack and leave piles or drawn cards alone. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deck_id": "string",
      "remaining": 1,
      "shuffled": true,
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
| `remaining` | number | Cards remaining in the deck. |
| `shuffled` | boolean | Whether the deck was shuffled. |
| `success` | boolean | Whether the deck operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/{{deck_id}}/shuffle/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reshuffle-deck.md) for the provider-specific parameters and requirements.

