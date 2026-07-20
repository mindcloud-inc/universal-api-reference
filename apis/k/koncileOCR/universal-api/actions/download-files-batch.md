# Koncile OCR: Download Files Batch



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/download-files-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/download-files-batch?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/download-files-batch?${params}`, {
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
| `document_ids[]` | array<number> | no | A list of document IDs to download as a ZIP archive. Accepts multiple values as an array. |
| `task_ids[]` | array<string> | no | A list of task IDs to resolve and download as a ZIP archive. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_ids": [
        1
      ],
      "task_ids": [
        "string"
      ],
      "zip_content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_ids` | array<number> | The requested document identifiers included in the ZIP batch. |
| `task_ids` | array<string> | The requested task identifiers included in the ZIP batch. |
| `zip_content` | string | The ZIP archive content returned by the endpoint. |

## Native endpoint

Through the native Koncile OCR API, this operation is `POST /fetch_files_batch` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-files-batch.md) for the provider-specific parameters and requirements.

