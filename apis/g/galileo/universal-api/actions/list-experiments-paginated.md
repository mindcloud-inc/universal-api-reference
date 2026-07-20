# Galileo: List Experiments Paginated

Finds experiments for a Galileo project with pagination.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-experiments-paginated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-experiments-paginated?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-experiments-paginated?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "experiments": [
        {
          "aggregateFeedback": {},
          "aggregateMetrics": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "createdByUser": {},
          "dataset": {},
          "id": "string",
          "name": "Ava Chen",
          "numSpans": 1,
          "numTraces": 1,
          "playground": {},
          "playgroundId": "string",
          "projectId": "string",
          "prompt": {},
          "promptModel": "string",
          "promptRunSettings": {},
          "rank": 1,
          "rankingScore": 1,
          "ratingAggregates": {},
          "status": {},
          "structuredAggregateMetrics": {},
          "tags": {},
          "taskType": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "winner": true
        }
      ],
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "startingToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `experiments` | array<object> |  |
| `experiments[].aggregateFeedback` | object |  |
| `experiments[].aggregateMetrics` | object |  |
| `experiments[].createdAt` | date |  |
| `experiments[].createdBy` | string |  |
| `experiments[].createdByUser` | object |  |
| `experiments[].dataset` | object |  |
| `experiments[].id` | string |  |
| `experiments[].name` | string |  |
| `experiments[].numSpans` | number |  |
| `experiments[].numTraces` | number |  |
| `experiments[].playground` | object |  |
| `experiments[].playgroundId` | string |  |
| `experiments[].projectId` | string |  |
| `experiments[].prompt` | object |  |
| `experiments[].promptModel` | string |  |
| `experiments[].promptRunSettings` | object |  |
| `experiments[].rank` | number |  |
| `experiments[].rankingScore` | number |  |
| `experiments[].ratingAggregates` | object |  |
| `experiments[].status` | object |  |
| `experiments[].structuredAggregateMetrics` | object |  |
| `experiments[].tags` | object |  |
| `experiments[].taskType` | number |  |
| `experiments[].updatedAt` | date |  |
| `experiments[].winner` | boolean |  |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `startingToken` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/experiments/paginated` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experiments-paginated.md) for the provider-specific parameters and requirements.

