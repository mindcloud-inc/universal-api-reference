# Bolna: List Agent Batches

Retrieves all batches for a specific Bolna agent.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-agent-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-agent-batches?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-agent-batches?${params}`, {
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
| `agentId` | string | yes | The ID of the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "executionStatus": {},
      "fileName": "Ava Chen",
      "fromPhoneNumber": "string",
      "humanizedCreatedAt": "string",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalContacts": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "validContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string |  |
| `createdAt` | date |  |
| `executionStatus` | object |  |
| `fileName` | string |  |
| `fromPhoneNumber` | string |  |
| `humanizedCreatedAt` | string |  |
| `scheduledAt` | date |  |
| `status` | string |  |
| `totalContacts` | number |  |
| `updatedAt` | date |  |
| `validContacts` | number |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /batches/:agentId/all` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-batches.md) for the provider-specific parameters and requirements.

