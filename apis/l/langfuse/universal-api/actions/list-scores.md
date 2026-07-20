# Langfuse: List Scores

Retrieves scores from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-scores?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-scores?${params}`, {
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
| `configId` | string | no |  |
| `datasetRunId` | string | no |  |
| `dataType` | string | no |  |
| `environment` | string | no |  |
| `fields` | string | no |  |
| `filter` | string | no |  |
| `fromTimestamp` | string | no |  |
| `name` | string | no |  |
| `observationId` | string | no |  |
| `operator` | string | no |  |
| `queueId` | string | no |  |
| `scoreIds` | string | no |  |
| `sessionId` | string | no |  |
| `source` | string | no |  |
| `toTimestamp` | string | no |  |
| `traceId` | string | no |  |
| `traceTags` | string | no |  |
| `userId` | string | no |  |
| `value` | string | no |  |

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

Through the native Langfuse API, this operation is `GET /v2/scores` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scores.md) for the provider-specific parameters and requirements.

