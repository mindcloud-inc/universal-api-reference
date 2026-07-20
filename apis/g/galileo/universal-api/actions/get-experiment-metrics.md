# Galileo: Get Experiment Metrics

Retrieves metrics for a Galileo experiment.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-experiment-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-experiment-metrics?connectionId=$CONNECTION_ID&experimentId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-experiment-metrics?${params}`, {
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
| `experimentId` | string | yes | Galileo experiment UUID. |
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metrics": [
        {
          "average": 1,
          "buckets": {},
          "dataType": "string",
          "name": "Ava Chen",
          "rollUpMethod": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metrics` | array<object> |  |
| `metrics[].average` | number |  |
| `metrics[].buckets` | object |  |
| `metrics[].dataType` | string |  |
| `metrics[].name` | string |  |
| `metrics[].rollUpMethod` | string |  |

## Native endpoint

Through the native Galileo API, this operation is `POST /v2/projects/:project_id/experiments/:experiment_id/metrics` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-metrics.md) for the provider-specific parameters and requirements.

