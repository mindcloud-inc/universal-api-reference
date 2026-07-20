# Upload to URL: Get File Information



```
GET https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/get-file-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upload to URL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/get-file-information?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/get-file-information?${params}`, {
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
| `fileId` | string | yes | The unique identifier of the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "2026-05-07T12:00:00.000Z",
      "file_size": 1,
      "filename": "Ava Chen",
      "id": "string",
      "is_expired": true,
      "mime_type": "string",
      "public_url": "https://example.com",
      "retention_days": 1,
      "uploaded_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | date |  |
| `file_size` | number |  |
| `filename` | string |  |
| `id` | string |  |
| `is_expired` | boolean |  |
| `mime_type` | string |  |
| `public_url` | string |  |
| `retention_days` | number |  |
| `uploaded_at` | date |  |

## Native endpoint

Through the native Upload to URL API, this operation is `GET /api/file/:file_id` (base URL `https://uploadtourl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-information.md) for the provider-specific parameters and requirements.

