# KnowledgeOwl: Update Category



```
PUT https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `nameEn` | string | no |  |
| `visibility` | string | no | Default: `public`. |
| `status` | string | no | Default: `active`. |

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

Through the native KnowledgeOwl API, this operation is `PUT /category/:id.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

