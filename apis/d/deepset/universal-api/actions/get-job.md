# Deepset: Get Job

Retrieves a job from a Deepset workspace.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-job?${params}`, {
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
| `jobId` | string | yes | deepset job ID. |
| `workspaceId` | string | yes | deepset workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "job_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `job_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v2/workspaces/:workspace_id/jobs/:job_id` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

