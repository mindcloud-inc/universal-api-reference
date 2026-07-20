# Monday Universal API Examples

These examples use the MindCloud API key and Monday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Boards With items

Retrieves items and their subitems from a Monday board by column value.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards-with-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards-with-items?${params}`, {
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
      "accountId": 1,
      "id": "string",
      "itemsPage": {
        "items": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "itemTerminology": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Boards With items action reference](actions/get-boards-with-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monday/latest/actions/get-boards-with-items).

## Create Sub Item

Creates a new subitem in Monday.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monday/latest/actions/create-sub-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monday/latest/actions/create-sub-item', {
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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Sub Item action reference](actions/create-sub-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monday/latest/actions/create-sub-item).
