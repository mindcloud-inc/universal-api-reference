# HiDrive: List Share Uploads

Retrieves share uploads from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-share-uploads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-share-uploads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-share-uploads?${params}`, {
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
| `fields` | string | no | Comma-separated share upload fields to include. |
| `id` | string | no | Share upload ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "created": 1,
      "has_password": true,
      "id": "string",
      "last_modified": 1,
      "maxcount": 1,
      "maxsize": 1,
      "path": "string",
      "pid": "string",
      "status": "string",
      "ttl": 1,
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Usage count. |
| `created` | number | Creation timestamp. |
| `has_password` | boolean | Whether the share upload is password protected. |
| `id` | string | Share upload ID. |
| `last_modified` | number | Last modified timestamp. |
| `maxcount` | number | Maximum usage count. |
| `maxsize` | number | Maximum upload size. |
| `path` | string | Upload target path. |
| `pid` | string | Path-independent object ID. |
| `status` | string | Share upload status. |
| `ttl` | number | Time-to-live in seconds. |
| `type` | string | Target item type. |
| `uri` | string | Share upload URI. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /shareupload` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-share-uploads.md) for the provider-specific parameters and requirements.

