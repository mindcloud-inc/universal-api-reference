# Bolna: Get Agent

Retrieves a specific Bolna voice AI agent.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-agent?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-agent?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The unique agent ID from Bolna. |

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
      "callingGuardrails": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inboundPhoneNumber": "string",
      "ingestSourceConfig": {},
      "restricted": true,
      "tasks": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhookUrl": "https://example.com"
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
| `callingGuardrails` | object |  |
| `createdAt` | date |  |
| `id` | string |  |
| `inboundPhoneNumber` | string |  |
| `ingestSourceConfig` | object |  |
| `restricted` | boolean |  |
| `tasks` | array<object> |  |
| `updatedAt` | date |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /v2/agent/:agentId` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

