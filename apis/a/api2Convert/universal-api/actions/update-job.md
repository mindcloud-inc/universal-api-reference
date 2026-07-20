# Api2Convert: Update Job

Updates an existing job in Api2Convert.

```
PUT https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "job": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "job": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | Unique identifier of the job to update. |
| `job` | object | yes | Full job payload used to update the job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversion": [
        {}
      ],
      "created_at": "string",
      "errors": [
        {}
      ],
      "fail_on_conversion_error": true,
      "fail_on_input_error": true,
      "id": "string",
      "input": [
        {}
      ],
      "modified_at": "string",
      "notify_status": true,
      "output": [
        {}
      ],
      "process": true,
      "status": {},
      "token": "string",
      "type": "string",
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversion` | array<object> | Conversions attached to the job. |
| `created_at` | string | Creation timestamp. |
| `errors` | array<object> | Job errors. |
| `fail_on_conversion_error` | boolean | Whether conversion failures should fail the job. |
| `fail_on_input_error` | boolean | Whether input failures should fail the job. |
| `id` | string | Unique identifier for the job. |
| `input` | array<object> | Input files attached to the job. |
| `modified_at` | string | Last modification timestamp. |
| `notify_status` | boolean | Whether status notifications are enabled. |
| `output` | array<object> | Output files generated for the job. |
| `process` | boolean | Whether the job should process automatically. |
| `status` | object | Current job status object. |
| `token` | string | Job token. |
| `type` | string | Job type. |
| `warnings` | array<object> | Job warnings. |

## Native endpoint

Through the native Api2Convert API, this operation is `PATCH /jobs/:job_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

