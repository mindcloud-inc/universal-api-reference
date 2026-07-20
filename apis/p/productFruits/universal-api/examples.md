# Product Fruits Universal API Examples

These examples use the MindCloud API key and Product Fruits connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Knowledge Base Categories



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-categories?${params}`, {
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
      "contents": [
        {
          "description": "string",
          "lang": "string",
          "slug": "string",
          "slug_state": "string",
          "title": "string"
        }
      ],
      "correlationId": "string",
      "icon": "string",
      "id": 1,
      "isFeatured": true,
      "order": 1,
      "parentCategoryId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Knowledge Base Categories action reference](actions/list-knowledge-base-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productFruits/latest/actions/list-knowledge-base-categories).

## Create Feedback



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "username": "Ava Chen"
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
      "authorName": "Ava Chen",
      "authorProps": "string",
      "authorUsername": "Ava Chen",
      "environmentInfo": "string",
      "id": 1,
      "isNative": true,
      "isSolved": true,
      "screenshots": [
        {}
      ],
      "sentAt": "2026-05-07T12:00:00.000Z",
      "text": "string",
      "videos": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Feedback action reference](actions/create-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productFruits/latest/actions/create-feedback).
