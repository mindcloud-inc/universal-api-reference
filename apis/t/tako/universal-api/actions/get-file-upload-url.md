# Tako: Get File Upload URL

Retrieves a file upload URL from Tako.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-file-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-file-upload-url?connectionId=$CONNECTION_ID&fileName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-file-upload-url?${params}`, {
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
| `fileName` | string | yes | Name of the file you plan to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "file_id": "string",
      "key": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object | Form fields required to complete the upload. |
| `file_id` | string | Generated Tako file ID. |
| `key` | string | Storage key for the uploaded file. |
| `url` | string | Presigned upload URL. |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/beta/file_upload_url` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-upload-url.md) for the provider-specific parameters and requirements.

