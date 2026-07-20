# Erase.bg: Delete Files

Deletes multiple files from Erase.bg storage.

```
DELETE https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-files?connectionId=$CONNECTION_ID&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-files?${params}`, {
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
| `ids[]` | array<string> | yes | Array of file _ids to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "_id": "string",
          "access": "string",
          "assetType": "string",
          "context": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "fileId": "string",
          "format": "string",
          "isActive": true,
          "name": "Ava Chen",
          "path": "string",
          "size": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Deleted files returned by the API. |
| `items[]._id` | string |  |
| `items[].access` | string |  |
| `items[].assetType` | string |  |
| `items[].context` | object |  |
| `items[].createdAt` | date |  |
| `items[].fileId` | string |  |
| `items[].format` | string |  |
| `items[].isActive` | boolean |  |
| `items[].name` | string |  |
| `items[].path` | string |  |
| `items[].size` | number |  |
| `items[].updatedAt` | date |  |
| `items[].url` | string |  |

## Native endpoint

Through the native Erase.bg API, this operation is `POST /service/platform/assets/v1.0/files/delete` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-files.md) for the provider-specific parameters and requirements.

