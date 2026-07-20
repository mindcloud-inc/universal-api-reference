# InsightIQ Universal API Examples

These examples use the MindCloud API key and InsightIQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Work Platforms

Retrieves available work platforms from InsightIQ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-work-platforms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-work-platforms?${params}`, {
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
      "data": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

See the full [List Work Platforms action reference](actions/list-work-platforms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightIQ/latest/actions/list-work-platforms).

## Create Async Content Comments Fetch

Creates an async content comments fetch request in InsightIQ.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-content-comments-fetch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentUrl": "https://example.com",
  "workPlatformId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-content-comments-fetch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentUrl": "https://example.com",
    "workPlatformId": "string"
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
      "content_url": "https://example.com",
      "id": "string",
      "max_results": 1,
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Async Content Comments Fetch action reference](actions/create-async-content-comments-fetch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightIQ/latest/actions/create-async-content-comments-fetch).
