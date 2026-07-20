# Erase.bg: Upload Asset From URL

Creates a file in Erase.bg from a URL.

```
POST https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/upload-asset-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/upload-asset-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/upload-asset-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name to store the asset under. |
| `path` | string | no | Destination folder path. |
| `url` | string | yes | Public URL of the asset to import. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "access": "string",
      "assetType": "string",
      "context": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileId": "string",
      "format": "string",
      "height": 1,
      "isActive": true,
      "kvStore": [
        {}
      ],
      "meta": {},
      "metadata": {},
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `access` | string |  |
| `assetType` | string |  |
| `context` | object |  |
| `createdAt` | date |  |
| `fileId` | string |  |
| `format` | string |  |
| `height` | number |  |
| `isActive` | boolean |  |
| `kvStore` | array<object> |  |
| `meta` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `path` | string |  |
| `size` | number |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Erase.bg API, this operation is `POST /service/platform/assets/v1.0/upload/url` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-asset-from-url.md) for the provider-specific parameters and requirements.

