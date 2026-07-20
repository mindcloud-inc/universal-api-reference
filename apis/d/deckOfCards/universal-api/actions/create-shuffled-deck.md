# Deck of Cards: Create Shuffled Deck

Creates a shuffled deck in Deck of Cards.

```
POST https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/create-shuffled-deck
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/create-shuffled-deck" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/create-shuffled-deck', {
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
| `deck_count` | number | no | Number of standard decks to include. Defaults to 1. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cards` | string | no | Optional comma-separated card codes for a partial deck, such as AS,2S,KS. |

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

Through the native Deck of Cards API, this operation is `GET deck/new/shuffle/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shuffled-deck.md) for the provider-specific parameters and requirements.

