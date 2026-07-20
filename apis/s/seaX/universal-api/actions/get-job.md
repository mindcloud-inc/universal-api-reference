# SeaX: Get Job

Retrieves a job from the current SeaX workspace.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-job?${params}`, {
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
| `jobId` | string | yes | Job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "ended_at": "string",
      "enqueued_at": "string",
      "error_code": 1,
      "error_msg": "string",
      "error_parameters": {},
      "job_id": "string",
      "started_at": "string",
      "status": {},
      "timeout": 1,
      "updated_at": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `ended_at` | string |  |
| `enqueued_at` | string |  |
| `error_code` | number |  |
| `error_msg` | string |  |
| `error_parameters` | object |  |
| `job_id` | string |  |
| `started_at` | string |  |
| `status` | object |  |
| `timeout` | number |  |
| `updated_at` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `GET /jobs/{job_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

