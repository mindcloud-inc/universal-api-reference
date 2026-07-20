# Reflect Universal API Examples

These examples use the MindCloud API key and Reflect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Reflect.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reflect/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "graphIds": [
        "string"
      ],
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reflect/latest/actions/get-current-user).

## Append to Daily Note

Appends text to a daily note in Reflect.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/append-to-daily-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "graphId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reflect/latest/actions/append-to-daily-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "graphId": "string",
    "text": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Append to Daily Note action reference](actions/append-to-daily-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reflect/latest/actions/append-to-daily-note).
