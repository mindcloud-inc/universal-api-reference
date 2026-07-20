# Kazm: Get Transform Job Metrics

Retrieves transform job metrics from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-transform-job-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-transform-job-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-transform-job-metrics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "steps": [
        {}
      ],
      "total_duration_seconds": 1,
      "total_input_rows": 1,
      "total_output_rows": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `steps` | array<object> |  |
| `total_duration_seconds` | number |  |
| `total_input_rows` | number |  |
| `total_output_rows` | number |  |

## Native endpoint

Through the native Kazm API, this operation is `GET /transform-jobs/:jobId/metrics` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transform-job-metrics.md) for the provider-specific parameters and requirements.

