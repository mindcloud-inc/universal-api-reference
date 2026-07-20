# Stack AI: Create Custom Tool



```
POST https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-custom-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-custom-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-custom-tool', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "color": "string",
      "connections": {},
      "deprecation_info": {},
      "description": "string",
      "headers": {},
      "icon": "string",
      "name": "Ava Chen",
      "openapi_schema": "string",
      "provider_group": [
        "string"
      ],
      "provider_id": "string",
      "provider_version": "string",
      "tags": [
        "string"
      ],
      "triggers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `color` | string |  |
| `connections` | object |  |
| `deprecation_info` | object |  |
| `description` | string |  |
| `headers` | object |  |
| `icon` | string |  |
| `name` | string |  |
| `openapi_schema` | string |  |
| `provider_group` | array<string> |  |
| `provider_id` | string |  |
| `provider_version` | string |  |
| `tags` | array<string> |  |
| `triggers` | array<object> |  |

## Native endpoint

Through the native Stack AI API, this operation is `POST /tools/custom` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-tool.md) for the provider-specific parameters and requirements.

