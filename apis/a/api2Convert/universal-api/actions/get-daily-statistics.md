# Api2Convert: Get Daily Statistics

Retrieves statistics for a specific day from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-daily-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-daily-statistics?connectionId=$CONNECTION_ID&day=string&filter=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "day": "string",
  "filter": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-daily-statistics?${params}`, {
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
| `day` | string | yes | Day in yyyy-mm-dd format. |
| `filter` | string | yes | Statistics scope filter: single or all. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_jobs": "string",
      "conversion_minutes": "string",
      "created_at": "string",
      "failed_jobs": "string",
      "input_traffic": "string",
      "job_counter": "string",
      "output_traffic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_jobs` | string | Number of completed jobs. |
| `conversion_minutes` | string | Conversion minutes consumed. |
| `created_at` | string | Statistics bucket timestamp. |
| `failed_jobs` | string | Number of failed jobs. |
| `input_traffic` | string | Input traffic amount. |
| `job_counter` | string | Number of jobs in the bucket. |
| `output_traffic` | string | Output traffic amount. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /stats/day/:day/:filter` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-statistics.md) for the provider-specific parameters and requirements.

