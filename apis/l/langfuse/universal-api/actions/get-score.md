# Langfuse: Get Score

Retrieves a score from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-score?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-score?${params}`, {
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
| `scoreId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorUserId": "string",
      "comment": "string",
      "configId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datasetRunId": "string",
      "dataType": "string",
      "environment": "string",
      "id": "string",
      "metadata": "string",
      "name": "Ava Chen",
      "observationId": "string",
      "queueId": "string",
      "sessionId": "string",
      "source": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "traceId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorUserId` | string |  |
| `comment` | string |  |
| `configId` | string |  |
| `createdAt` | date |  |
| `datasetRunId` | string |  |
| `dataType` | string |  |
| `environment` | string |  |
| `id` | string |  |
| `metadata` | string |  |
| `name` | string |  |
| `observationId` | string |  |
| `queueId` | string |  |
| `sessionId` | string |  |
| `source` | string |  |
| `timestamp` | date |  |
| `traceId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Langfuse API, this operation is `GET /v2/scores/:scoreId` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-score.md) for the provider-specific parameters and requirements.

