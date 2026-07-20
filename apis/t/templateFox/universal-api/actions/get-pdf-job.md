# TemplateFox: Get PDF Job

Retrieves a PDF job from TemplateFox.

```
GET https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-pdf-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TemplateFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-pdf-job?connectionId=$CONNECTION_ID&jobId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-pdf-job?${params}`, {
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
| `jobId` | string | yes | Async PDF job ID. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": "string",
      "created_at": "string",
      "error_code": "string",
      "error_message": "string",
      "export_type": "string",
      "filename": "Ava Chen",
      "id": "string",
      "result_expires_at": "string",
      "result_filename": "Ava Chen",
      "result_s3_bucket": "string",
      "result_s3_key": "string",
      "result_url": "https://example.com",
      "status": "string",
      "store_s3": true,
      "template_id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | string |  |
| `created_at` | string |  |
| `error_code` | string |  |
| `error_message` | string |  |
| `export_type` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `result_expires_at` | string |  |
| `result_filename` | string |  |
| `result_s3_bucket` | string |  |
| `result_s3_key` | string |  |
| `result_url` | string |  |
| `status` | string |  |
| `store_s3` | boolean |  |
| `template_id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native TemplateFox API, this operation is `GET /v1/pdf/jobs/{{job_id}}` (base URL `https://api.templatefox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-job.md) for the provider-specific parameters and requirements.

