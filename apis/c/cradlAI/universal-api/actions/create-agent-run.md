# Cradl AI: Create Agent Run

Creates a new agent run in Cradl AI.

```
POST https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | Identifier of the agent that owns the run. |
| `variables` | object | no | Variables passed to the agent run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "events": [
        {}
      ],
      "resourceIds": [
        "string"
      ],
      "runId": "string",
      "status": "string",
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z",
      "variablesFileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Agent identifier. |
| `createdBy` | string | User who created the run. |
| `createdTime` | date | Timestamp when the run was created. |
| `events` | array<object> | Events produced by the run. |
| `resourceIds` | array<string> | Resources associated with the run. |
| `runId` | string | Run identifier. |
| `status` | string | Run status. |
| `updatedBy` | string | User who last updated the run. |
| `updatedTime` | date | Timestamp when the run was last updated. |
| `variablesFileUrl` | string | URL to the run variables file. |

## Native endpoint

Through the native Cradl AI API, this operation is `POST /agents/:agentId/runs` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-run.md) for the provider-specific parameters and requirements.

