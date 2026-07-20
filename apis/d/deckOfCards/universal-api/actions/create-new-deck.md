# Deck of Cards: Create New Deck

Creates a new deck in Deck of Cards.

```
POST https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/create-new-deck
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/create-new-deck" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/create-new-deck', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jokers_enabled` | boolean | no | Include two jokers in the new deck when true. Default: `false`. |

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
| `deck_id` | string | Identifier for the created deck. |
| `remaining` | number | Cards remaining in the deck. |
| `shuffled` | boolean | Whether the deck was shuffled. |
| `success` | boolean | Whether the deck operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/new/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-deck.md) for the provider-specific parameters and requirements.

