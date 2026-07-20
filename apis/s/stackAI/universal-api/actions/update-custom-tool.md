# Stack AI: Update Custom Tool



```
PUT https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/update-custom-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/update-custom-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "providerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/update-custom-tool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "providerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `providerId` | string | yes | The provider identifier. |

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
| `actions` | array<object> | Action definitions exposed by the custom tool provider. |
| `color` | string | Accent color for the custom tool provider. |
| `connections` | object | Available connection information when present. |
| `deprecation_info` | object | Deprecation metadata when present. |
| `description` | string | The custom tool provider description. |
| `headers` | object | Header schema metadata when present. |
| `icon` | string | The custom tool provider icon URL. |
| `name` | string | The custom tool provider name. |
| `openapi_schema` | string | Stored OpenAPI schema when present. |
| `provider_group` | array<string> | Provider group classifications. |
| `provider_id` | string | The custom tool provider identifier. |
| `provider_version` | string | The custom tool provider version when present. |
| `tags` | array<string> | Tags associated with the custom tool provider. |
| `triggers` | array<object> | Trigger definitions exposed by the custom tool provider. |

## Native endpoint

Through the native Stack AI API, this operation is `PUT /tools/custom/:provider_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-tool.md) for the provider-specific parameters and requirements.

