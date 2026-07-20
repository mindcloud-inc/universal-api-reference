# HiDrive: Create Share Link

Creates a new share link in HiDrive.

```
POST https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-share-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-share-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-share-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `password` | string | no | Optional private share link password. |
| `path` | string | no | File path for the share link. |
| `pid` | string | no | File public ID for the share link. |
| `ttl` | number | no | Share link expiry in seconds. |
| `maxcount` | number | no | Allowed successful downloads. |

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
      "path": "string",
      "pid": "string",
      "size": 1,
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
| `has_password` | boolean | Whether the share link is password protected. |
| `id` | string | Share link ID. |
| `last_modified` | number | Last modified timestamp. |
| `maxcount` | number | Maximum usage count. |
| `path` | string | Shared path. |
| `pid` | string | Path-independent object ID. |
| `size` | number | Shared file size when returned. |
| `status` | string | Share link status. |
| `ttl` | number | Time-to-live in seconds. |
| `type` | string | Shared item type. |
| `uri` | string | Share link URL. |

## Native endpoint

Through the native HiDrive API, this operation is `POST /sharelink` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-share-link.md) for the provider-specific parameters and requirements.

