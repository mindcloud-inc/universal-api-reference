# Files.com: Get File Download Link

Retrieves a file download link from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-file-download-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-file-download-link?connectionId=$CONNECTION_ID&path=sample.txt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "sample.txt"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-file-download-link?${params}`, {
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
| `path` | string | yes | File path without leading or trailing slashes. Default: `sample.txt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "download_uri": "string",
      "mime_type": "string",
      "mtime": "2026-05-07T12:00:00.000Z",
      "path": "string",
      "permissions": "string",
      "region": "string",
      "size": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `display_name` | string |  |
| `download_uri` | string |  |
| `mime_type` | string |  |
| `mtime` | date |  |
| `path` | string |  |
| `permissions` | string |  |
| `region` | string |  |
| `size` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /files/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-download-link.md) for the provider-specific parameters and requirements.

