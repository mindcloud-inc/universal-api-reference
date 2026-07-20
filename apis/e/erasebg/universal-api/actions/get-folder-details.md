# Erase.bg: Get Folder Details

Retrieves folder details from Erase.bg storage.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-folder-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-folder-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-folder-details?${params}`, {
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
| `name` | string | no | Folder name to inspect. |
| `path` | string | no | Folder path to inspect. |

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
      "isOriginal": true,
      "kvStore": [
        {}
      ],
      "meta": {},
      "metadata": {},
      "name": "Ava Chen",
      "orgId": "string",
      "path": "string",
      "size": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `isOriginal` | boolean |  |
| `kvStore` | array<object> |  |
| `meta` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `orgId` | string |  |
| `path` | string |  |
| `size` | number |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `width` | number |  |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/assets/v1.0/folders` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-details.md) for the provider-specific parameters and requirements.

