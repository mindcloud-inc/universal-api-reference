# Deck of Cards: List Pile Cards

Retrieves cards in a pile from Deck of Cards.

```
GET https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/list-pile-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deck of Cards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/list-pile-cards?connectionId=$CONNECTION_ID&deck_id=string&pile_name=discard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deck_id": "string",
  "pile_name": "discard"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deckOfCards/latest/actions/list-pile-cards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deck_id` | string | yes | Deck identifier returned by a create deck action. |
| `pile_name` | string | yes | Pile name to list. Default: `discard`. |

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
| `piles` | object | Pile state and cards keyed by pile name. |
| `remaining` | number | Cards remaining in the main deck. |
| `success` | boolean | Whether the pile list operation succeeded. |

## Native endpoint

Through the native Deck of Cards API, this operation is `GET deck/{{deck_id}}/pile/{{pile_name}}/list/` (base URL `https://www.deckofcardsapi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pile-cards.md) for the provider-specific parameters and requirements.

