# DocumentPro: Get Large Upload URL

Retrieves a large-file upload URL from DocumentPro.

```
GET https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/get-large-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/get-large-upload-url?connectionId=$CONNECTION_ID&file_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/get-large-upload-url?${params}`, {
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
| `file_name` | string | yes | The original file name for the large upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "upload_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | string |  |
| `upload_url` | string |  |

## Native endpoint

Through the native DocumentPro API, this operation is `GET /v1/documents/upload_url` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-large-upload-url.md) for the provider-specific parameters and requirements.

