# Deck of Cards Universal API Examples

These examples use the MindCloud API key and Deck of Cards connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pile Cards

Retrieves cards in a pile from Deck of Cards.

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

Example response:

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

See the full [List Pile Cards action reference](actions/list-pile-cards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deckOfCards/latest/actions/list-pile-cards).

## Add Cards to Pile

Adds cards to a pile in Deck of Cards.

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

Example response:

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

See the full [Add Cards to Pile action reference](actions/add-cards-to-pile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deckOfCards/latest/actions/add-cards-to-pile).
