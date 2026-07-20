# Orq.ai: List Agents

Retrieves a list of agents from Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/list-agents?${params}`, {
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
      "data": [
        {
          "created": "string",
          "description": "string",
          "instructions": "string",
          "key": "string",
          "model": {
            "id": "string"
          },
          "path": "string",
          "role": "string",
          "status": "string",
          "type": "string",
          "updated": "string",
          "version": "string"
        }
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created` | string |  |
| `data[].description` | string |  |
| `data[].instructions` | string |  |
| `data[].key` | string |  |
| `data[].model.id` | string |  |
| `data[].path` | string |  |
| `data[].role` | string |  |
| `data[].status` | string |  |
| `data[].type` | string |  |
| `data[].updated` | string |  |
| `data[].version` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `GET /v2/agents` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

