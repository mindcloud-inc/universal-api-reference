# Unstructured: Get Failed Files

Retrieves failed files for a job from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-failed-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-failed-files?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-failed-files?${params}`, {
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
      "failedFiles": [
        [
          {}
        ]
      ],
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failedFiles[]` | array<object> | Failed files and failure details. |
| `jobId` | string | Job ID. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /jobs/:job_id/failed-files` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-failed-files.md) for the provider-specific parameters and requirements.

