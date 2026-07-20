# Instapaper Universal API Examples

These examples use the MindCloud API key and Instapaper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Credentials



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/verify-credentials?${params}`, {
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
      "type": "string",
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Verify Credentials action reference](actions/verify-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instapaper/latest/actions/verify-credentials).

## Add Bookmark



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/add-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/add-bookmark', {
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
  "data": [
    {
      "bookmarkId": 1,
      "description": "string",
      "hash": "string",
      "progress": 1,
      "progressTimestamp": 1,
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Bookmark action reference](actions/add-bookmark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instapaper/latest/actions/add-bookmark).
