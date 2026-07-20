# TemplateFox: List PDF Jobs

Retrieves PDF jobs from TemplateFox.

```
GET https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/list-pdf-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TemplateFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/list-pdf-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/list-pdf-jobs?${params}`, {
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
| `limit` | number | no | Number of jobs to return. Example: `20`. |
| `offset` | number | no | Number of jobs to skip. Example: `0`. |
| `status` | string | no | Optional job status filter. Example: `completed`. |

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

Through the native TemplateFox API, this operation is `GET /v1/pdf/jobs` (base URL `https://api.templatefox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pdf-jobs.md) for the provider-specific parameters and requirements.

