# UserBit Universal API Examples

These examples use the MindCloud API key and UserBit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves accessible workspaces from the UserBit account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-workspaces?${params}`, {
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
      "id": "string",
      "label": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userBit/latest/actions/list-workspaces).

## Create Or Update Note

Creates or updates a note in UserBit.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-or-update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-or-update-note', {
  method: 'PUT',
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
  "data": [
    {
      "htmlContent": "string",
      "id": "string",
      "sourceType": "string",
      "textContent": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Note action reference](actions/create-or-update-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userBit/latest/actions/create-or-update-note).
