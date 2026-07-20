# ConvertHub: Cancel Job

Cancels an active conversion job in ConvertHub.

```
DELETE https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/cancel-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/cancel-job?connectionId=$CONNECTION_ID&jobId=job_123e4567-e89b-12d3-a456-426614174000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_123e4567-e89b-12d3-a456-426614174000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/cancel-job?${params}`, {
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
| `jobId` | string | yes | Example: `job_123e4567-e89b-12d3-a456-426614174000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string |  |
| `message` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `DELETE /v2/jobs/:jobId` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-job.md) for the provider-specific parameters and requirements.

