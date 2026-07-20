# GraphHopper: Get Route Optimization Solution

Retrieves a route optimization solution from GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-route-optimization-solution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-route-optimization-solution?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-route-optimization-solution?${params}`, {
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
| `jobId` | string | yes | Route optimization job ID. |

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
| `job_id` | string | Route optimization job identifier. |
| `processing_time` | number | Processing time in milliseconds. |
| `solution` | object | Optimization solution. |
| `status` | string | Optimization job status. |
| `waiting_time_in_queue` | number | Queue wait time in milliseconds. |

## Native endpoint

Through the native GraphHopper API, this operation is `GET /vrp/solution/:jobId` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-optimization-solution.md) for the provider-specific parameters and requirements.

