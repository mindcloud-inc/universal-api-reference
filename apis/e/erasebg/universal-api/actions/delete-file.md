# Erase.bg: Delete File

Deletes a file from Erase.bg storage.

```
DELETE https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | Combination of path and name of the file. |

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

Through the native Erase.bg API, this operation is `DELETE /service/platform/assets/v1.0/files/:fileId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

