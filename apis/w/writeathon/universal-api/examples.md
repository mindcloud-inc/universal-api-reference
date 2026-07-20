# Writeathon Universal API Examples

These examples use the MindCloud API key and Writeathon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Writeathon.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-current-user?${params}`, {
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
      "data": {
        "id": "string",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/writeathon/latest/actions/get-current-user).

## Append Card

Appends content to an existing Writeathon card.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/append-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/append-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "content": "string"
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
      "action": "string",
      "data": "string"
    }
  ],
  "meta": {}
}
```

See the full [Append Card action reference](actions/append-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/writeathon/latest/actions/append-card).
