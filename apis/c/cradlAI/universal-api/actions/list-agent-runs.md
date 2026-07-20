# Cradl AI: List Agent Runs

Retrieves all agent runs from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agent-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agent-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agent-runs?${params}`, {
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
| `agentId` | string | yes | Identifier of the agent whose runs to list. |
| `history` | string | no | History filter for runs. |
| `status` | string | no | Status filter for runs. |
| `sort` | string | no | Sort order for runs. |
| `createdTimeAfter` | date | no | Return runs created after this timestamp. |
| `createdTimeBefore` | date | no | Return runs created before this timestamp. |
| `updatedTimeAfter` | date | no | Return runs updated after this timestamp. |
| `updatedTimeBefore` | date | no | Return runs updated before this timestamp. |

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

Through the native Cradl AI API, this operation is `GET /agents/:agentId/runs` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agent-runs.md) for the provider-specific parameters and requirements.

