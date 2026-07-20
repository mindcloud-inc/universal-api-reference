# Cradl AI: Get Agent

Retrieves an agent from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-agent?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-agent?${params}`, {
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
| `agentId` | string | yes | Identifier of the agent to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "metadata": {},
      "name": "Ava Chen",
      "resourceIds": [
        "string"
      ],
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Agent identifier. |
| `createdBy` | string | User who created the agent. |
| `createdTime` | date | Timestamp when the agent was created. |
| `description` | string | Agent description. |
| `metadata` | object | Metadata attached to the agent. |
| `name` | string | Agent name. |
| `resourceIds` | array<string> | Resource identifiers attached to the agent. |
| `updatedBy` | string | User who last updated the agent. |
| `updatedTime` | date | Timestamp when the agent was last updated. |

## Native endpoint

Through the native Cradl AI API, this operation is `GET /agents/:agentId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

