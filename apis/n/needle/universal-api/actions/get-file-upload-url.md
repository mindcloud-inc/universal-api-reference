# Needle: Get File Upload URL

Retrieves a signed file upload URL from Needle.

```
GET https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-file-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Needle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-file-upload-url?connectionId=$CONNECTION_ID&contentType=application%2Fpdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentType": "application/pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-file-upload-url?${params}`, {
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
| `contentType` | string | yes | MIME type to generate an upload URL for Default: `application/pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "uploadUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `uploadUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Needle API, this operation is `GET /api/v1/files/upload_url` (base URL `https://needle.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-upload-url.md) for the provider-specific parameters and requirements.

