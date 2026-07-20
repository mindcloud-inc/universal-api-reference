# Freepik Universal API Examples

These examples use the MindCloud API key and Freepik connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Resources

Finds Freepik resources by search term and filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-resources?${params}`, {
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
      "active": true,
      "author": {},
      "filename": "Ava Chen",
      "id": 1,
      "image": {},
      "licenses": [
        {}
      ],
      "meta": {},
      "products": [
        {}
      ],
      "related": {},
      "stats": {},
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Search Resources action reference](actions/search-resources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freepik/latest/actions/search-resources).

## Improve Prompt



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/improve-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "A detailed photo of a sunlit forest path",
  "type": "image"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freepik/latest/actions/improve-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "A detailed photo of a sunlit forest path",
    "type": "image"
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
      "generated": [
        {}
      ],
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Improve Prompt action reference](actions/improve-prompt.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freepik/latest/actions/improve-prompt).
