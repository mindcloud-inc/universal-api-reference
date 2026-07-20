# HiDrive: Create Share Upload

Creates a new share upload in HiDrive.

```
POST https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-share-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-share-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-share-upload', {
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
| `password` | string | no | Optional private share upload password. |
| `path` | string | no | Directory path for the share upload. |
| `pid` | string | no | Directory public ID for the share upload. |
| `ttl` | number | no | Share upload expiry in seconds. |
| `maxcount` | number | no | Allowed upload count. |
| `maxsize` | number | no | Maximum upload file size in bytes. |

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
| `path` | string | Upload target path. |
| `pid` | string | Path-independent object ID. |
| `status` | string | Share upload status. |
| `ttl` | number | Time-to-live in seconds. |
| `type` | string | Target item type. |
| `uri` | string | Share upload URI. |

## Native endpoint

Through the native HiDrive API, this operation is `POST /shareupload` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-share-upload.md) for the provider-specific parameters and requirements.

