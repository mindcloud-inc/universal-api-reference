# KnowledgeOwl: Create Article



```
POST https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `name` | string | yes |  |
| `currentVersionTitle` | string | yes |  |
| `currentVersionText` | string | yes |  |
| `status` | string | yes | Default: `draft`. |
| `visibility` | string | yes | Default: `public`. |
| `urlHash` | string | yes |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.current_version` | object |  |
| `data.current_version.en` | object |  |
| `data.current_version.en.text` | string |  |
| `data.current_version.en.title` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.pdf` | boolean |  |
| `data.project_id` | string |  |
| `data.searchTitle` | string |  |
| `data.status` | string |  |
| `data.summary` | string |  |
| `data.type` | string |  |
| `data.url_hash` | string |  |
| `data.visibility` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native KnowledgeOwl API, this operation is `POST /article.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-article.md) for the provider-specific parameters and requirements.

