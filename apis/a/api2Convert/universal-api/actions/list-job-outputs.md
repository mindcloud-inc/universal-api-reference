# Api2Convert: List Job Outputs

Retrieves output files for a job from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-outputs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-outputs?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-outputs?${params}`, {
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
| `jobId` | string | yes | Unique identifier of the job whose output files should be listed. |
| `conversionId` | string | no | Filter output files by conversion identifier. |
| `inputId` | string | no | Filter output files by input identifier. |

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

Through the native Api2Convert API, this operation is `GET /jobs/:job_id/output` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-outputs.md) for the provider-specific parameters and requirements.

