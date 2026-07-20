# SVAHNAR: List All Agents

Retrieves all agents from SVAHNAR.

```
GET https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/list-all-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/list-all-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/list-all-agents?${params}`, {
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
      "agents": [
        {}
      ],
      "request_metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | array<object> | List of agents the authenticated user can access. |
| `request_metadata` | object | Response metadata including the request ID. |

## Native endpoint

Through the native SVAHNAR API, this operation is `GET /v1/agents/list-agents` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-agents.md) for the provider-specific parameters and requirements.

