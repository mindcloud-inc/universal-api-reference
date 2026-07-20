# Api2Convert: Get Job Output

Retrieves an output file from a job in Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-output
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-output?connectionId=$CONNECTION_ID&jobId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-output?${params}`, {
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
| `jobId` | string | yes | ID of the job that owns the output file. |
| `fileId` | string | yes | ID of the output file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checksum": "string",
      "content_type": "string",
      "created_at": "string",
      "downloads_counter": 1,
      "filename": "Ava Chen",
      "id": "string",
      "metadata": {},
      "size": 1,
      "source": {},
      "status": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum` | string | Output file checksum. |
| `content_type` | string | Output file MIME type. |
| `created_at` | string | Creation timestamp. |
| `downloads_counter` | number | Number of downloads for the output file. |
| `filename` | string | Output file name. |
| `id` | string | Output file identifier. |
| `metadata` | object | Output file metadata. |
| `size` | number | Output file size in bytes. |
| `source` | object | Output source information. |
| `status` | string | Output file status. |
| `uri` | string | Download URI for the output file. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /jobs/:job_id/output/:file_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-output.md) for the provider-specific parameters and requirements.

