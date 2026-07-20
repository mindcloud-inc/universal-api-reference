# Website Toolbox Community Universal API Examples

These examples use the MindCloud API key and Website Toolbox Community connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Categories



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/list-categories?${params}`, {
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
      "has_more": true,
      "object": "string",
      "page": 1,
      "size": 1,
      "total_size": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Categories action reference](actions/list-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/websiteToolboxCommunity/latest/actions/list-categories).

## Create Category



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/create-category', {
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
      "categoryId": 1,
      "description": "string",
      "heading": "string",
      "isPrivate": true,
      "linked": "https://example.com",
      "locked": true,
      "object": "string",
      "parentId": 1,
      "passwordProtected": true,
      "title": "string",
      "unlisted": true
    }
  ],
  "meta": {}
}
```

See the full [Create Category action reference](actions/create-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/websiteToolboxCommunity/latest/actions/create-category).
