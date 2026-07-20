# Api2Convert: List Jobs

Retrieves active job records from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-jobs?${params}`, {
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
| `status` | string | no | Filter jobs by status code. |
| `page` | string | no | Page number for paginated job results. |

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

Through the native Api2Convert API, this operation is `GET /jobs` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

