# Koncile OCR: Download File



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/download-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/download-file?${params}`, {
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
| `document_id` | number | no | Download the original file for this document ID. |
| `task_id` | string | no | Download the original file by task ID when document_id is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": 1,
      "file_content": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | number | The document identifier used to download the file. |
| `file_content` | string | The downloaded file content returned by the endpoint. |
| `task_id` | string | The task identifier used to download the file. |

## Native endpoint

Through the native Koncile OCR API, this operation is `GET /fetch_file` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

