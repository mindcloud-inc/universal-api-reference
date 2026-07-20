# Api2Convert: Create Job Input

Creates an input file for a job in Api2Convert.

```
POST https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job-input" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "inputFile": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job-input', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "inputFile": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | Unique identifier of the job that will receive the input file. |
| `inputFile` | object | yes | Input file payload describing the source file to attach to the job. |

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

Through the native Api2Convert API, this operation is `POST /jobs/:job_id/input` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-input.md) for the provider-specific parameters and requirements.

