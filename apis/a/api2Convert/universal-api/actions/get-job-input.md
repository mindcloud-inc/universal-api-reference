# Api2Convert: Get Job Input

Retrieves an input file from a job in Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-input?connectionId=$CONNECTION_ID&jobId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-input?${params}`, {
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
| `jobId` | string | yes | ID of the job. |
| `fileId` | string | yes | ID of the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checksum": "string",
      "content_type": "string",
      "created_at": "string",
      "credentials": [
        {}
      ],
      "engine": "string",
      "filename": "Ava Chen",
      "hash": "string",
      "id": "string",
      "metadata": {},
      "modified_at": "string",
      "options": {},
      "parameters": [
        {}
      ],
      "size": 1,
      "source": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum` | string | Input file checksum. |
| `content_type` | string | Input file MIME type. |
| `created_at` | string | Creation timestamp. |
| `credentials` | array<object> | Stored credentials for the input file. |
| `engine` | string | Download engine used for the input file. |
| `filename` | string | Input file name. |
| `hash` | string | Input file hash. |
| `id` | string | Input file identifier. |
| `metadata` | object | Input file metadata. |
| `modified_at` | string | Last modification timestamp. |
| `options` | object | Input file options. |
| `parameters` | array<object> | Additional input parameters. |
| `size` | number | Input file size in bytes. |
| `source` | string | Source URI or identifier for the input file. |
| `status` | string | Input file status. |
| `type` | string | How the input file was provided. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /jobs/:job_id/input/:file_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-input.md) for the provider-specific parameters and requirements.

