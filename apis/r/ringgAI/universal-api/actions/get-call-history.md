# Ringg AI: Get Call History

Retrieves call history from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-call-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-call-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-call-history?${params}`, {
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
| `startDate` | date | no | Filter calls starting from this date (ISO 8601 format with timezone). |
| `endDate` | date | no | Filter calls up to this date (ISO 8601 format with timezone). |
| `agentId` | string | no | Filter calls by assistant ID. |
| `status` | string | no | Filter calls by status. |
| `bulkListId` | string | no | Filter calls by bulk list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calls": [
        {
          "agent": {
            "agentName": "Ava Chen",
            "id": "string"
          },
          "audioRecording": "string",
          "callAttemptTime": "2026-05-07T12:00:00.000Z",
          "callCost": 1,
          "callDuration": 1,
          "callType": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "inboundFrom": "string",
          "name": "Ava Chen",
          "status": "string",
          "subStatus": "string",
          "toNumber": "string",
          "transcript": "string"
        }
      ],
      "count": 1,
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calls` | array<object> |  |
| `calls[].agent` | object |  |
| `calls[].agent.agentName` | string |  |
| `calls[].agent.id` | string |  |
| `calls[].audioRecording` | string |  |
| `calls[].callAttemptTime` | date |  |
| `calls[].callCost` | number |  |
| `calls[].callDuration` | number |  |
| `calls[].callType` | string |  |
| `calls[].createdAt` | date |  |
| `calls[].id` | string |  |
| `calls[].inboundFrom` | string |  |
| `calls[].name` | string |  |
| `calls[].status` | string | The current status of the call |
| `calls[].subStatus` | string | The sub-status of the call providing more detail on the call outcome |
| `calls[].toNumber` | string |  |
| `calls[].transcript` | string |  |
| `count` | number |  |
| `limit` | number |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /calling/history` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-call-history.md) for the provider-specific parameters and requirements.

