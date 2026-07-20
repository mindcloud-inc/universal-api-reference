# HoneyHive: Get Experiment Result

Retrieves an experiment result from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-experiment-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-experiment-result?connectionId=$CONNECTION_ID&runId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-experiment-result?${params}`, {
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
| `runId` | string | yes | Run ID. |
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
      "datapoints": [
        {}
      ],
      "failed": true,
      "metrics": {
        "aggregationFunction": "string",
        "details": {}
      },
      "passed": true,
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datapoints` | array<object> |  |
| `failed` | boolean |  |
| `metrics` | object |  |
| `metrics.aggregationFunction` | string |  |
| `metrics.details` | object |  |
| `passed` | boolean |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /runs/{run_id}/result` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-result.md) for the provider-specific parameters and requirements.

