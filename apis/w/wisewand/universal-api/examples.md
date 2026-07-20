# Wisewand Universal API Examples

These examples use the MindCloud API key and Wisewand connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List projects

Retrieves projects from your Wisewand workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-projects?${params}`, {
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
      "count": 1,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wisewand/latest/actions/list-projects).

## Create a feed

Creates a new feed in your Wisewand workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-a-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/feed.xml"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-a-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/feed.xml"
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

See the full [Create a feed action reference](actions/create-a-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wisewand/latest/actions/create-a-feed).
