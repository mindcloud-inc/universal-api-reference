# Bolna: List Agents

Retrieves all voice AI agents in your Bolna account.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-agents?${params}`, {
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
      "agentName": "Ava Chen",
      "agentPrompts": {},
      "agentStatus": "string",
      "agentType": "string",
      "agentWelcomeMessage": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inboundPhoneNumber": "string",
      "restricted": true,
      "tasks": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentName` | string |  |
| `agentPrompts` | object |  |
| `agentStatus` | string |  |
| `agentType` | string |  |
| `agentWelcomeMessage` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `inboundPhoneNumber` | string |  |
| `restricted` | boolean |  |
| `tasks` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /v2/agent/all` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

