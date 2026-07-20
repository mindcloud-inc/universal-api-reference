# AssignX: List Agents

Retrieves agents you can access in AssignX.

```
GET https://connect.mindcloud.co/v1/universal/assignX/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assignX/latest/actions/list-agents?${params}`, {
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
      "agentType": "string",
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "Id": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "websiteEmbeddingKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentType` | string |  |
| `avatar` | string |  |
| `createdAt` | date |  |
| `creator` | string |  |
| `Id` | string |  |
| `lastActivity` | date |  |
| `name` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |
| `websiteEmbeddingKey` | string |  |

## Native endpoint

Through the native AssignX API, this operation is `GET agents` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

