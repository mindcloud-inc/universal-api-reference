# Galileo: Get Trace

Retrieves a trace from Galileo by ID.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-trace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-trace?connectionId=$CONNECTION_ID&projectId=string&traceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "traceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-trace?${params}`, {
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
| `traceId` | string | yes | Galileo trace UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": "string",
      "output": "string",
      "redactedInput": "string",
      "redactedOutput": "string",
      "spans": [
        {
          "agentType": "string",
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
          "output": "string",
          "parentId": "string",
          "projectId": "string",
          "redactedInput": "string",
          "redactedOutput": "string",
          "runId": "string",
          "sessionBatchId": "string",
          "sessionId": "string",
          "spans": [
            {
              "agentType": "string",
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
              "output": "string",
              "parentId": "string",
              "projectId": "string",
              "redactedInput": "string",
              "redactedOutput": "string",
              "runId": "string",
              "sessionBatchId": "string",
              "sessionId": "string",
              "spans": [
                {}
              ],
              "statusCode": 1,
              "stepNumber": 1,
              "tags": [
                "string"
              ],
              "traceId": "string",
              "type": "string",
              "updatedAt": "2026-05-07T12:00:00.000Z",
              "userMetadata": {}
            }
          ],
          "statusCode": 1,
          "stepNumber": 1,
          "tags": [
            "string"
          ],
          "traceId": "string",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userMetadata": {}
        }
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input` | string |  |
| `output` | string |  |
| `redactedInput` | string |  |
| `redactedOutput` | string |  |
| `spans` | array<object> |  |
| `spans[].agentType` | string |  |
| `spans[].annotationAggregates` | object |  |
| `spans[].annotationQueueIds` | array<string> |  |
| `spans[].annotations` | object |  |
| `spans[].createdAt` | date |  |
| `spans[].datasetInput` | string |  |
| `spans[].datasetMetadata` | object |  |
| `spans[].datasetOutput` | string |  |
| `spans[].externalId` | string |  |
| `spans[].feedbackRatingInfo` | object |  |
| `spans[].fileIds` | array<string> |  |
| `spans[].fileModalities` | array<string> |  |
| `spans[].files` | object |  |
| `spans[].hasChildren` | boolean |  |
| `spans[].id` | string |  |
| `spans[].input` | string |  |
| `spans[].isComplete` | boolean |  |
| `spans[].metricInfo` | object |  |
| `spans[].metrics` | object |  |
| `spans[].metricsBatchId` | string |  |
| `spans[].name` | string |  |
| `spans[].output` | string |  |
| `spans[].parentId` | string |  |
| `spans[].projectId` | string |  |
| `spans[].redactedInput` | string |  |
| `spans[].redactedOutput` | string |  |
| `spans[].runId` | string |  |
| `spans[].sessionBatchId` | string |  |
| `spans[].sessionId` | string |  |
| `spans[].spans` | array<object> |  |
| `spans[].spans[].agentType` | string |  |
| `spans[].spans[].annotationAggregates` | object |  |
| `spans[].spans[].annotationQueueIds` | array<string> |  |
| `spans[].spans[].annotations` | object |  |
| `spans[].spans[].createdAt` | date |  |
| `spans[].spans[].datasetInput` | string |  |
| `spans[].spans[].datasetMetadata` | object |  |
| `spans[].spans[].datasetOutput` | string |  |
| `spans[].spans[].externalId` | string |  |
| `spans[].spans[].feedbackRatingInfo` | object |  |
| `spans[].spans[].fileIds` | array<string> |  |
| `spans[].spans[].fileModalities` | array<string> |  |
| `spans[].spans[].files` | object |  |
| `spans[].spans[].hasChildren` | boolean |  |
| `spans[].spans[].id` | string |  |
| `spans[].spans[].input` | string |  |
| `spans[].spans[].isComplete` | boolean |  |
| `spans[].spans[].metricInfo` | object |  |
| `spans[].spans[].metrics` | object |  |
| `spans[].spans[].metricsBatchId` | string |  |
| `spans[].spans[].name` | string |  |
| `spans[].spans[].output` | string |  |
| `spans[].spans[].parentId` | string |  |
| `spans[].spans[].projectId` | string |  |
| `spans[].spans[].redactedInput` | string |  |
| `spans[].spans[].redactedOutput` | string |  |
| `spans[].spans[].runId` | string |  |
| `spans[].spans[].sessionBatchId` | string |  |
| `spans[].spans[].sessionId` | string |  |
| `spans[].spans[].spans` | array<object> |  |
| `spans[].spans[].statusCode` | number |  |
| `spans[].spans[].stepNumber` | number |  |
| `spans[].spans[].tags` | array<string> |  |
| `spans[].spans[].traceId` | string |  |
| `spans[].spans[].type` | string |  |
| `spans[].spans[].updatedAt` | date |  |
| `spans[].spans[].userMetadata` | object |  |
| `spans[].statusCode` | number |  |
| `spans[].stepNumber` | number |  |
| `spans[].tags` | array<string> |  |
| `spans[].traceId` | string |  |
| `spans[].type` | string |  |
| `spans[].updatedAt` | date |  |
| `spans[].userMetadata` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/traces/:trace_id` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trace.md) for the provider-specific parameters and requirements.

