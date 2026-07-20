# HiDrive: Get File Download URL

Retrieves a file download URL from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-file-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-file-download-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-file-download-url?${params}`, {
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
| `path` | string | no | File path. |
| `pid` | string | no | File public ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | number | Expiration timestamp when provided. |
| `url` | string | Temporary streaming/download URL for the file. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /file/url` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-download-url.md) for the provider-specific parameters and requirements.

