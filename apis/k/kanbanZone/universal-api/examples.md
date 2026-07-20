# Kanban Zone Universal API Examples

These examples use the MindCloud API key and Kanban Zone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Boards

Retrieves boards from Kanban Zone.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-boards?${params}`, {
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
      "boards": [
        {}
      ],
      "count": 1,
      "errors": {}
    }
  ],
  "meta": {}
}
```

See the full [List Boards action reference](actions/list-boards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kanbanZone/latest/actions/list-boards).

## Add Cards

Creates cards in Kanban Zone.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/add-cards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "string",
  "cards[].title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/add-cards', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "string",
    "cards[].title": "string"
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
      "cards": [
        {}
      ],
      "cardsAdded": 1,
      "errors": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Cards action reference](actions/add-cards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kanbanZone/latest/actions/add-cards).
