# Bolna: List All Agent Executions

Retrieves execution records for a specific Bolna agent.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-all-agent-executions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-all-agent-executions?connectionId=$CONNECTION_ID&limit=25&offset=0&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-all-agent-executions?${params}`, {
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
| `answeredByVoiceMail` | boolean | no | Optional voicemail filter. |
| `batchId` | string | no | Optional batch ID filter. |
| `callType` | string | no | Optional call-direction filter. |
| `from` | date | no | Optional lower UTC datetime bound for execution creation time. |
| `provider` | string | no | Optional conversation-provider filter. |
| `status` | string | no | Optional execution status filter. |
| `to` | date | no | Optional upper UTC datetime bound for execution creation time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "answeredByVoiceMail": true,
      "batchId": "string",
      "batchRunDetails": {},
      "contextDetails": {},
      "conversationTime": 1,
      "costBreakdown": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "errorMessage": "string",
      "extractedData": {},
      "fromNumber": "string",
      "id": "string",
      "recordingUrl": "https://example.com",
      "status": "string",
      "toNumber": "string",
      "totalCost": 1,
      "transcript": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `answeredByVoiceMail` | boolean |  |
| `batchId` | string |  |
| `batchRunDetails` | object |  |
| `contextDetails` | object |  |
| `conversationTime` | number |  |
| `costBreakdown` | object |  |
| `createdAt` | date |  |
| `errorMessage` | string |  |
| `extractedData` | object |  |
| `fromNumber` | string |  |
| `id` | string |  |
| `recordingUrl` | string |  |
| `status` | string |  |
| `toNumber` | string |  |
| `totalCost` | number |  |
| `transcript` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /v2/agent/:agentId/executions` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-agent-executions.md) for the provider-specific parameters and requirements.

