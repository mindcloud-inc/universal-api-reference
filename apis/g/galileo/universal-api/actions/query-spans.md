# Galileo: Query Spans

Finds spans in a Galileo project by filters.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-spans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-spans?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-spans?${params}`, {
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
| `projectId` | string | yes | Galileo project UUID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logStreamId` | string | no | Optional Galileo log stream UUID. Provide exactly one of Log Stream ID, Experiment ID, or Metrics Testing ID. |
| `experimentId` | string | no | Optional Galileo experiment UUID. Provide exactly one of Log Stream ID, Experiment ID, or Metrics Testing ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastRowId": "string",
      "limit": 1,
      "nextStartingToken": 1,
      "numRecords": 1,
      "paginated": true,
      "records": [
        {
          "annotationAggregates": {},
          "annotationQueueIds": [
            "string"
          ],
          "annotations": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "datasetInput": "string",
          "datasetMetadata": {},
          "datasetOutput": "string",
          "externalId": "string",
          "feedbackRatingInfo": {},
          "fileIds": [
            "string"
          ],
          "fileModalities": [
            "string"
          ],
          "files": {},
          "hasChildren": true,
          "id": "string",
          "input": "string",
          "isComplete": true,
          "metricInfo": {},
          "metrics": {},
          "metricsBatchId": "string",
          "name": "Ava Chen",
          "numSpans": 1,
          "output": "string",
          "projectId": "string",
          "redactedInput": "string",
          "redactedOutput": "string",
          "runId": "string",
          "sessionBatchId": "string",
          "sessionId": "string",
          "statusCode": 1,
          "tags": [
            "string"
          ],
          "traceId": "string",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userMetadata": {}
        }
      ],
      "startingToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastRowId` | string |  |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `numRecords` | number |  |
| `paginated` | boolean |  |
| `records` | array<object> |  |
| `records[].annotationAggregates` | object |  |
| `records[].annotationQueueIds` | array<string> |  |
| `records[].annotations` | object |  |
| `records[].createdAt` | date |  |
| `records[].datasetInput` | string |  |
| `records[].datasetMetadata` | object |  |
| `records[].datasetOutput` | string |  |
| `records[].externalId` | string |  |
| `records[].feedbackRatingInfo` | object |  |
| `records[].fileIds` | array<string> |  |
| `records[].fileModalities` | array<string> |  |
| `records[].files` | object |  |
| `records[].hasChildren` | boolean |  |
| `records[].id` | string |  |
| `records[].input` | string |  |
| `records[].isComplete` | boolean |  |
| `records[].metricInfo` | object |  |
| `records[].metrics` | object |  |
| `records[].metricsBatchId` | string |  |
| `records[].name` | string |  |
| `records[].numSpans` | number |  |
| `records[].output` | string |  |
| `records[].projectId` | string |  |
| `records[].redactedInput` | string |  |
| `records[].redactedOutput` | string |  |
| `records[].runId` | string |  |
| `records[].sessionBatchId` | string |  |
| `records[].sessionId` | string |  |
| `records[].statusCode` | number |  |
| `records[].tags` | array<string> |  |
| `records[].traceId` | string |  |
| `records[].type` | string |  |
| `records[].updatedAt` | date |  |
| `records[].userMetadata` | object |  |
| `startingToken` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `POST /v2/projects/:project_id/spans/search` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-spans.md) for the provider-specific parameters and requirements.

