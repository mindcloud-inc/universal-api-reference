# HiDrive: List Share Links

Retrieves share links from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-share-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-share-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-share-links?${params}`, {
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
| `fields` | string | no | Comma-separated share link fields to include. |
| `id` | string | no | Share link ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "created": 1,
      "id": "string",
      "last_modified": 1,
      "maxcount": 1,
      "password": "string",
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
| `id` | string | Share link ID. |
| `last_modified` | number | Last modified timestamp. |
| `maxcount` | number | Maximum usage count. |
| `password` | string | Password marker when returned. |
| `path` | string | Shared path. |
| `pid` | string | Path-independent object ID. |
| `status` | string | Share link status. |
| `ttl` | number | Time-to-live in seconds. |
| `type` | string | Shared item type. |
| `uri` | string | Share link URL. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /sharelink` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-share-links.md) for the provider-specific parameters and requirements.

