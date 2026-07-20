# Extruct AI: Resume Discovery Task

Resumes a discovery task in Extruct AI.

```
PUT https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/resume-discovery-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/resume-discovery-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task_id": "00000000-0000-0000-0000-000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/resume-discovery-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task_id": "00000000-0000-0000-0000-000000000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task_id` | string | yes | Deep Search task identifier. Example: `00000000-0000-0000-0000-000000000000`. |
| `desiredNewResults` | number | no | Additional result count to request. Default: `25`. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoDataSources": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "criteria": [
        {}
      ],
      "dataSources": [
        "string"
      ],
      "desiredNumResults": 1,
      "id": "string",
      "isExhausted": true,
      "numResults": 1,
      "numResultsDiscovered": 1,
      "numResultsEnriched": 1,
      "numResultsEvaluated": 1,
      "query": "string",
      "status": "string",
      "tableId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoDataSources` | boolean |  |
| `createdAt` | date |  |
| `criteria` | array<object> |  |
| `dataSources` | array<string> |  |
| `desiredNumResults` | number |  |
| `id` | string |  |
| `isExhausted` | boolean |  |
| `numResults` | number |  |
| `numResultsDiscovered` | number |  |
| `numResultsEnriched` | number |  |
| `numResultsEvaluated` | number |  |
| `query` | string |  |
| `status` | string |  |
| `tableId` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `POST /v1/discovery_tasks/:task_id/resume` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-discovery-task.md) for the provider-specific parameters and requirements.

