# Dify: Get Annotation Reply Job Status

Retrieves annotation reply job status from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-annotation-reply-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-annotation-reply-job-status?connectionId=$CONNECTION_ID&action=string&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "action": "string",
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-annotation-reply-job-status?${params}`, {
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
| `action` | string | yes | Annotation reply action. |
| `jobId` | string | yes | Annotation reply job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMsg": "string",
      "jobId": "string",
      "jobStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMsg` | string |  |
| `jobId` | string |  |
| `jobStatus` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /apps/annotation-reply/:action/status/:job_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-annotation-reply-job-status.md) for the provider-specific parameters and requirements.

