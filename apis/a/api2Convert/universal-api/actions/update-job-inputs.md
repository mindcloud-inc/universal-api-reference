# Api2Convert: Update Job Inputs

Updates input files for a job in Api2Convert.

```
PUT https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job-inputs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job-inputs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "inputFilePatch": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job-inputs', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "inputFilePatch": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | Unique identifier of the job whose inputs should be updated. |
| `inputFilePatch` | object | yes | Patch payload for the job input collection. |

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

Through the native Api2Convert API, this operation is `PATCH /jobs/:job_id/input` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-inputs.md) for the provider-specific parameters and requirements.

