# Pinboard Universal API Examples

These examples use the MindCloud API key and Pinboard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Latest Bookmark Update



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/get-latest-bookmark-update?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/get-latest-bookmark-update?${params}`, {
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
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Latest Bookmark Update action reference](actions/get-latest-bookmark-update.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinboard/latest/actions/get-latest-bookmark-update).

## Add Bookmark



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/add-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/add-bookmark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "url": "https://example.com"
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
      "result_code": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Bookmark action reference](actions/add-bookmark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinboard/latest/actions/add-bookmark).
