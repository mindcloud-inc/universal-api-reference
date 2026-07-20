# GraphHopper: Solve Route Optimization Problem

Solves a route optimization problem in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/solve-route-optimization-problem
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/solve-route-optimization-problem?connectionId=$CONNECTION_ID&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/solve-route-optimization-problem?${params}`, {
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
| `requestBody` | object | yes | Route optimization request JSON body matching GraphHopper's Request schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "copyrights": [
        "string"
      ],
      "job_id": "string",
      "processing_time": 1,
      "solution": {},
      "status": "string",
      "waiting_time_in_queue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `copyrights` | array<string> | Attribution strings returned by GraphHopper. |
| `job_id` | string | Route optimization job identifier returned with the solved optimization response. |
| `processing_time` | number | Processing time in milliseconds. |
| `solution` | object | Optimization solution. |
| `status` | string | Optimization status. |
| `waiting_time_in_queue` | number | Queue wait time in milliseconds. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /vrp` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/solve-route-optimization-problem.md) for the provider-specific parameters and requirements.

