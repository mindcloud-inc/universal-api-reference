# Reamaze Universal API Examples

These examples use the MindCloud API key and Reamaze connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Conversations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-conversations?${params}`, {
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
      "conversations": [
        {}
      ],
      "pageCount": 1,
      "pageSize": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Conversations action reference](actions/list-conversations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reamaze/latest/actions/list-conversations).

## Create Article



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string",
  "article": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string",
    "article": {}
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
      "author": {},
      "body": "string",
      "createdAt": "string",
      "slug": "string",
      "status": 1,
      "title": "string",
      "topic": {},
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Article action reference](actions/create-article.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reamaze/latest/actions/create-article).
