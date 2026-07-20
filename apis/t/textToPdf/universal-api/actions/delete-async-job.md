# Text to pdf: Delete Async Job

Deletes an asynchronous job from Text to PDF.

```
DELETE https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/delete-async-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Text to pdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/delete-async-job?connectionId=$CONNECTION_ID&arguments=%5Bobject%20Object%5D&arguments.jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arguments": "[object Object]",
  "arguments.jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/delete-async-job?${params}`, {
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
| `arguments` | object | yes | Tool input arguments object. |
| `arguments.jobId` | string | yes | Unique asynchronous conversion job id to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "message": "string",
        "status_code": 1
      },
      "error": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.message` | string | Async job deletion confirmation or provider wrapper message. |
| `data.status_code` | number | Underlying ConvertAPI HTTP status code when returned by Composio. |
| `error` | string | Error message when execution fails. |
| `successful` | boolean | Whether the Composio tool execution succeeded. |

## Native endpoint

Through the native Text to pdf API, this operation is `POST /tools/execute/TEXT_TO_PDF_DELETE_ASYNC_JOB` (base URL `https://backend.composio.dev/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-async-job.md) for the provider-specific parameters and requirements.

