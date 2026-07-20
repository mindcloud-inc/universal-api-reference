# HiDrive: Update Share

Updates an existing share in HiDrive.

```
PUT https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-share
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-share" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-share', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Share ID to update. |
| `password` | string | no | Optional share password. |
| `ttl` | number | no | Share expiry in seconds. |
| `maxcount` | number | no | Maximum issued share tokens. |
| `writable` | boolean | no | Allow write access to the shared folder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "created": 1,
      "file_type": "string",
      "has_password": true,
      "id": "string",
      "is_encrypted": true,
      "maxcount": 1,
      "path": "string",
      "readable": true,
      "share_type": "string",
      "status": "string",
      "uri": "string",
      "writable": true
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
| `file_type` | string | Shared object file type. |
| `has_password` | boolean | Whether the share is password protected. |
| `id` | string | Share ID. |
| `is_encrypted` | boolean | Whether the share is encrypted. |
| `maxcount` | number | Maximum usage count. |
| `path` | string | Shared directory path. |
| `readable` | boolean | Whether the share is readable. |
| `share_type` | string | Type of share. |
| `status` | string | Share status. |
| `uri` | string | Share URI. |
| `writable` | boolean | Whether the share is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `PUT /share` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-share.md) for the provider-specific parameters and requirements.

