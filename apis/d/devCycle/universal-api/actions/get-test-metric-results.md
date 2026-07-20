# DevCycle: Get Test Metric Results

Retrieves test metric results from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-test-metric-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-test-metric-results?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-test-metric-results?${params}`, {
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
| `control` | string | no | Control variation key. Default: `on`. |
| `dimension` | string | no | Metric aggregation dimension. Default: `COUNT_PER_UNIQUE_USER`. |
| `endDate` | string | no | Inclusive ISO-8601 end timestamp. Default: `2026-04-02T20:30:00Z`. |
| `event` | string | no | Metric event name. Default: `Sign Ups`. |
| `feature` | string | no | Feature key. Default: `mindcloud-flag`. |
| `optimize` | string | no | Optimization direction. Default: `increase`. |
| `project` | string | no | Project key. Default: `mindcloud`. |
| `startDate` | string | no | Inclusive ISO-8601 start timestamp. Default: `2026-04-02T20:18:56Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "result": {
        "dataSeries": [
          [
            {}
          ]
        ],
        "variations": [
          [
            {}
          ]
        ]
      },
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `result.dataSeries[]` | array<object> |  |
| `result.variations[]` | array<object> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/test-metric-results` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test-metric-results.md) for the provider-specific parameters and requirements.

