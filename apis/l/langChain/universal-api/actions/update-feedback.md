# LangChain: Update Feedback



```
PUT https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedbackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedbackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedbackId` | string | yes | Feedback identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "comparativeExperimentId": {},
      "correction": {},
      "createdAt": "string",
      "extra": {
        "error": true
      },
      "feedbackGroupId": {},
      "feedbackSource": {},
      "feedbackThreadId": {},
      "id": "string",
      "isRoot": true,
      "key": "string",
      "modifiedAt": "string",
      "runId": "string",
      "score": 1,
      "sessionId": "string",
      "startTime": "string",
      "traceId": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `comparativeExperimentId` | object |  |
| `correction` | object |  |
| `createdAt` | string |  |
| `extra.error` | boolean |  |
| `feedbackGroupId` | object |  |
| `feedbackSource` | object |  |
| `feedbackThreadId` | object |  |
| `id` | string |  |
| `isRoot` | boolean |  |
| `key` | string |  |
| `modifiedAt` | string |  |
| `runId` | string |  |
| `score` | number |  |
| `sessionId` | string |  |
| `startTime` | string |  |
| `traceId` | string |  |
| `value` | object |  |

## Native endpoint

Through the native LangChain API, this operation is `PATCH /api/v1/feedback/:feedbackId` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feedback.md) for the provider-specific parameters and requirements.

