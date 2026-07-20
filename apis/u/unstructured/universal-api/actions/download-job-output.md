# Unstructured: Download Job Output

Downloads job output from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/download-job-output
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/download-job-output?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/download-job-output?${params}`, {
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
| `jobId` | string | yes | The job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com",
      "expiresAt": "string",
      "fileCount": 1,
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string | Download URL for job output. |
| `expiresAt` | string | Download expiration timestamp. |
| `fileCount` | number | Number of downloadable files. |
| `jobId` | string | Job ID. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /jobs/:job_id/download` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-job-output.md) for the provider-specific parameters and requirements.

