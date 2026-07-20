# Api2Convert: List Job Threads

Retrieves processing threads for a job from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-threads?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-threads?${params}`, {
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
| `jobId` | string | yes | Unique identifier of the job whose threads should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "exec_time": 1,
      "hash": "string",
      "info": "string",
      "modified_at": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Creation timestamp. |
| `exec_time` | number | Thread execution time in seconds. |
| `hash` | string | Thread identifier. |
| `info` | string | Additional thread information. |
| `modified_at` | string | Last modification timestamp. |
| `status` | number | Thread status code. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /jobs/:job_id/threads` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-threads.md) for the provider-specific parameters and requirements.

