# FutureAGI: Get Simulation Metrics



```
GET https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/get-simulation-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FutureAGI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/get-simulation-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/get-simulation-metrics?${params}`, {
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
| `executionId` | string | no | Execution ID. |
| `runTestName` | string | no | Run test name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `status` | boolean |  |

## Native endpoint

Through the native FutureAGI API, this operation is `GET /sdk/api/v1/simulation/metrics/` (base URL `https://api.futureagi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-simulation-metrics.md) for the provider-specific parameters and requirements.

