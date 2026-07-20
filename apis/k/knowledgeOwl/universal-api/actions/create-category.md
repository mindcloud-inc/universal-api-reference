# KnowledgeOwl: Create Category



```
POST https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "basic",
  "projectId": "string",
  "urlHash": "https://example.com",
  "nameEn": "Ava Chen",
  "visibility": "public",
  "status": "active"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "basic",
    "projectId": "string",
    "urlHash": "https://example.com",
    "nameEn": "Ava Chen",
    "visibility": "public",
    "status": "active"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Default: `basic`. |
| `projectId` | string | yes |  |
| `urlHash` | string | yes |  |
| `nameEn` | string | yes |  |
| `visibility` | string | yes | Default: `public`. |
| `status` | string | yes | Default: `active`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "faq_display": "string",
        "id": "string",
        "name": "Ava Chen",
        "project_id": "string",
        "status": "string",
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
| `data.faq_display` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.project_id` | string |  |
| `data.status` | string |  |
| `data.type` | string |  |
| `data.url_hash` | string |  |
| `data.visibility` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native KnowledgeOwl API, this operation is `POST /category.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

