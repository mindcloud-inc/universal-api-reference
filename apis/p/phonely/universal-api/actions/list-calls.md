# Phonely: List Calls

Retrieves calls for a Phonely agent.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-calls?${params}`, {
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
| `agentId` | string | yes | The ID of the agent whose calls you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abTestId": {},
      "abTestSuccess": true,
      "abTestType": {},
      "agentId": "string",
      "businessPhoneNumber": {},
      "campaignId": {},
      "cOutcome": "string",
      "cSentiment": "string",
      "cTopic": {},
      "customerPhoneNumber": {},
      "draftAgentId": {},
      "draftAgentVersion": {},
      "duration": 1,
      "endedAt": "string",
      "endedReason": "string",
      "id": "string",
      "mode": "string",
      "read": true,
      "recordingUrl": "https://example.com",
      "startedAt": "string",
      "status": "string",
      "type": "string",
      "workflowPathHistory": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abTestId` | object |  |
| `abTestSuccess` | boolean |  |
| `abTestType` | object |  |
| `agentId` | string |  |
| `businessPhoneNumber` | object |  |
| `campaignId` | object |  |
| `cOutcome` | string |  |
| `cSentiment` | string |  |
| `cTopic` | object |  |
| `customerPhoneNumber` | object |  |
| `draftAgentId` | object |  |
| `draftAgentVersion` | object |  |
| `duration` | number |  |
| `endedAt` | string |  |
| `endedReason` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `read` | boolean |  |
| `recordingUrl` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `type` | string |  |
| `workflowPathHistory` | object |  |

## Native endpoint

Through the native Phonely API, this operation is `GET /api/calls/{{agentId}}` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

