# Erase.bg: Update File

Updates a file in Erase.bg storage.

```
PUT https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/update-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | Combination of path and name of the file. |
| `isActive` | boolean | no | Whether the file should remain active. |
| `name` | string | no | Updated file name. |
| `path` | string | no | Updated folder path. |

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

Through the native Erase.bg API, this operation is `PATCH /service/platform/assets/v1.0/files/:fileId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file.md) for the provider-specific parameters and requirements.

