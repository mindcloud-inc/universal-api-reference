# Relevance AI: Create Tool



```
POST https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/create-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/create-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "title": "string",
  "toolId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/create-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "title": "string",
    "toolId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes |  |
| `public` | boolean | no | Default: `false`. |
| `title` | string | yes |  |
| `toolId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed_documents": [
        {}
      ],
      "inserted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed_documents` | array<object> |  |
| `inserted` | number |  |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /studios/bulk_update` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tool.md) for the provider-specific parameters and requirements.

