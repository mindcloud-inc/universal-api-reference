# Optimizely: Get Experiment Results

Retrieves results for an experiment in Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-experiment-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-experiment-results?connectionId=$CONNECTION_ID&experimentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-experiment-results?${params}`, {
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
| `experimentId` | string | yes | The experiment id to fetch results for. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidenceThreshold": 1,
      "endTime": "string",
      "experimentId": 1,
      "isStale": true,
      "metrics": [
        {}
      ],
      "reach": 1,
      "startTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidenceThreshold` | number |  |
| `endTime` | string |  |
| `experimentId` | number |  |
| `isStale` | boolean |  |
| `metrics` | array<object> |  |
| `reach` | number |  |
| `startTime` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /experiments/{experimentId}/results` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-results.md) for the provider-specific parameters and requirements.

