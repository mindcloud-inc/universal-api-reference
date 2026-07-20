# TranslatePlus: List I18n Jobs

Retrieves i18n translation jobs from TranslatePlus.

```
GET https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/list-i18n-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/list-i18n-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/list-i18n-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error_message": "string",
      "failed_keys": 1,
      "file_type": "string",
      "id": "string",
      "job_id": "string",
      "original_filename": "Ava Chen",
      "source_language": "string",
      "status": "string",
      "target_languages": [
        "string"
      ],
      "total_keys": 1,
      "translated_files": [
        {}
      ],
      "translated_keys": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | date |  |
| `created_at` | date |  |
| `error_message` | string |  |
| `failed_keys` | number |  |
| `file_type` | string |  |
| `id` | string |  |
| `job_id` | string |  |
| `original_filename` | string |  |
| `source_language` | string |  |
| `status` | string |  |
| `target_languages` | array<string> |  |
| `total_keys` | number |  |
| `translated_files` | array<object> |  |
| `translated_keys` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `GET /v2/translate/i18n/jobs` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-i18n-jobs.md) for the provider-specific parameters and requirements.

