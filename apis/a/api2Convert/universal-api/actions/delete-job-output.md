# Api2Convert: Delete Job Output

Deletes an output file from a job in Api2Convert.

```
DELETE https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job-output
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job-output?connectionId=$CONNECTION_ID&jobId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job-output?${params}`, {
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
| `jobId` | string | yes | Unique identifier of the job that owns the output file. |
| `fileId` | string | yes | Unique identifier of the output file to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "file_id": "string",
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
| `deleted` | boolean | Whether the output file was deleted. |
| `file_id` | string | Identifier of the deleted output file. |
| `job_id` | string | Identifier of the parent job. |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Api2Convert API, this operation is `DELETE /jobs/:job_id/output/:file_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job-output.md) for the provider-specific parameters and requirements.

