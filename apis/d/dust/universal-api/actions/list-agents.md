# Dust: List Agents

Retrieves agent configurations from the Dust workspace.

```
GET https://connect.mindcloud.co/v1/universal/dust/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dust/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dust/latest/actions/list-agents?${params}`, {
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
      "agentConfigurations": [
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
| `agentConfigurations` | array<object> | Agent configurations available in the Dust workspace. |

## Native endpoint

Through the native Dust API, this operation is `GET /api/v1/w/:workspaceId/assistant/agent_configurations` (base URL `https://dust.tt`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

