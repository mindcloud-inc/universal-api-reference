# Ringg AI: Get Workspace Numbers

Retrieves workspace numbers from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-numbers?${params}`, {
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
      "workspaceNumbers": [
        {
          "agent": {
            "agentDisplayName": "Ava Chen",
            "id": "string"
          },
          "callCount": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "isInboundEnabled": true,
          "number": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workspaceNumbers` | array<object> |  |
| `workspaceNumbers[].agent` | object |  |
| `workspaceNumbers[].agent.agentDisplayName` | string |  |
| `workspaceNumbers[].agent.id` | string |  |
| `workspaceNumbers[].callCount` | number |  |
| `workspaceNumbers[].createdAt` | date |  |
| `workspaceNumbers[].id` | string |  |
| `workspaceNumbers[].isInboundEnabled` | boolean |  |
| `workspaceNumbers[].number` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /workspace/numbers` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-workspace-numbers.md) for the provider-specific parameters and requirements.

