# LangChain: List Sessions



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/list-sessions?${params}`, {
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
| `limit` | number | no | Maximum number of sessions to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Number of sessions to skip. |
| `name` | string | no | Filter sessions by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completionCost": {},
      "completionTokens": {},
      "defaultDatasetId": {},
      "description": {},
      "endTime": {},
      "errorRate": {},
      "extra": {},
      "feedbackStats": {},
      "firstTokenP50": {},
      "firstTokenP99": {},
      "id": "string",
      "lastRunStartTime": {},
      "lastRunStartTimeLive": {},
      "latencyP50": {},
      "latencyP99": {},
      "name": "Ava Chen",
      "promptCost": {},
      "promptTokens": {},
      "referenceDatasetId": {},
      "runCount": {},
      "runFacets": {},
      "sessionFeedbackStats": {},
      "startTime": "string",
      "streamingRate": {},
      "tenantId": "string",
      "testRunNumber": {},
      "totalCost": {},
      "totalTokens": {},
      "traceTier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completionCost` | object |  |
| `completionTokens` | object |  |
| `defaultDatasetId` | object |  |
| `description` | object |  |
| `endTime` | object |  |
| `errorRate` | object |  |
| `extra` | object |  |
| `feedbackStats` | object |  |
| `firstTokenP50` | object |  |
| `firstTokenP99` | object |  |
| `id` | string |  |
| `lastRunStartTime` | object |  |
| `lastRunStartTimeLive` | object |  |
| `latencyP50` | object |  |
| `latencyP99` | object |  |
| `name` | string |  |
| `promptCost` | object |  |
| `promptTokens` | object |  |
| `referenceDatasetId` | object |  |
| `runCount` | object |  |
| `runFacets` | object |  |
| `sessionFeedbackStats` | object |  |
| `startTime` | string |  |
| `streamingRate` | object |  |
| `tenantId` | string |  |
| `testRunNumber` | object |  |
| `totalCost` | object |  |
| `totalTokens` | object |  |
| `traceTier` | string |  |

## Native endpoint

Through the native LangChain API, this operation is `GET /api/v1/sessions` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

