# HoneyHive: Get Experiment Comparison

Retrieves an experiment comparison from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-experiment-comparison
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-experiment-comparison?connectionId=$CONNECTION_ID&runId1=string&runId2=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId1": "string",
  "runId2": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-experiment-comparison?${params}`, {
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
| `runId1` | string | yes | First run ID. |
| `runId2` | string | yes | Second run ID. |
| `projectId` | string | yes | Project ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aggregateFunction` | string | no | Aggregate function. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commonDatapoints": [
        {}
      ],
      "eventDetails": {},
      "metrics": {},
      "oldRun": {
        "configuration": {},
        "createdAt": "string",
        "datapointIds": [
          "string"
        ],
        "datasetId": "string",
        "eventIds": [
          "string"
        ],
        "id": "string",
        "metadata": {},
        "name": "Ava Chen",
        "project": "string",
        "results": {},
        "runId": "string",
        "sessionIds": [
          "string"
        ],
        "status": "string",
        "tenant": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commonDatapoints` | array<object> |  |
| `eventDetails` | object |  |
| `metrics` | object |  |
| `oldRun` | object |  |
| `oldRun.configuration` | object |  |
| `oldRun.createdAt` | string |  |
| `oldRun.datapointIds` | array<string> |  |
| `oldRun.datasetId` | string |  |
| `oldRun.eventIds` | array<string> |  |
| `oldRun.id` | string |  |
| `oldRun.metadata` | object |  |
| `oldRun.name` | string |  |
| `oldRun.project` | string |  |
| `oldRun.results` | object |  |
| `oldRun.runId` | string |  |
| `oldRun.sessionIds` | array<string> |  |
| `oldRun.status` | string |  |
| `oldRun.tenant` | string |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /runs/{run_id_1}/compare-with/{run_id_2}` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-comparison.md) for the provider-specific parameters and requirements.

