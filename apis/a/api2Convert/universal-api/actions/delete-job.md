# Api2Convert: Delete Job

Cancels an existing job in Api2Convert.

```
DELETE https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job?${params}`, {
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
| `jobId` | string | yes | Unique identifier of the job to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "job_id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the job was deleted. |
| `job_id` | string | Identifier of the deleted job. |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Api2Convert API, this operation is `DELETE /jobs/:job_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

