# Stack AI: List Custom Tools



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-custom-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-custom-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-custom-tools?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Stack AI API, this operation is `GET /tools/custom` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-tools.md) for the provider-specific parameters and requirements.

