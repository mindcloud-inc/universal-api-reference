# Monday Universal API Examples

These examples use the MindCloud API key and Monday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Boards



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards?${params}`, {
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

See the full [Get Boards action reference](actions/get-boards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monday/latest/actions/get-boards).

## Create Item



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monday/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "123456",
  "itemName": "Test 1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monday/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "123456",
    "itemName": "Test 1234"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Item action reference](actions/create-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monday/latest/actions/create-item).
