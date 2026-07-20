# KnowledgeOwl Universal API Examples

These examples use the MindCloud API key and KnowledgeOwl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Categories



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/list-categories?${params}`, {
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
        [
          {}
        ]
      ],
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [List Categories action reference](actions/list-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/knowledgeOwl/latest/actions/list-categories).

## Create Article



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "currentVersionTitle": "string",
  "currentVersionText": "string",
  "status": "draft",
  "visibility": "public",
  "urlHash": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
    "currentVersionTitle": "string",
    "currentVersionText": "string",
    "status": "draft",
    "visibility": "public",
    "urlHash": "https://example.com"
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
      "data": {
        "current_version": {
          "en": {
            "text": "string",
            "title": "string"
          }
        },
        "id": "string",
        "name": "Ava Chen",
        "pdf": true,
        "project_id": "string",
        "searchTitle": "string",
        "status": "string",
        "summary": "string",
        "type": "string",
        "url_hash": "https://example.com",
        "visibility": "string"
      },
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [Create Article action reference](actions/create-article.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/knowledgeOwl/latest/actions/create-article).
