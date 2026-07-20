# Erase.bg: List Files

Retrieves files from Erase.bg storage by search filters.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/list-files?${params}`, {
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
| `format` | string | no | Filter by file format. |
| `name` | string | no | Find items with a matching name. |
| `onlyFiles` | boolean | no | Fixed Stage 1 test-action query flag for PixelBin listFiles. Default: `false`. |
| `path` | string | no | Find items in the specified path. |
| `onlyFolders` | boolean | no | Fixed Stage 1 test-action query flag for PixelBin listFiles. Default: `false`. |
| `pageNo` | number | no | Fixed Stage 1 page number for the Erase.bg connection test action. Default: `1`. |
| `pageSize` | number | no | Fixed Stage 1 page size for the Erase.bg connection test action. Default: `10`. |
| `sort` | string | no | Fixed Stage 1 sort field for the Erase.bg connection test action. Default: `name`. |

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
      ],
      "page": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Files returned by the query. |
| `items[]._id` | string |  |
| `items[].access` | string |  |
| `items[].assetType` | string |  |
| `items[].createdAt` | date |  |
| `items[].fileId` | string |  |
| `items[].format` | string |  |
| `items[].isActive` | boolean |  |
| `items[].name` | string |  |
| `items[].path` | string |  |
| `items[].size` | number |  |
| `items[].updatedAt` | date |  |
| `items[].url` | string |  |
| `page` | object | Pagination metadata. |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/assets/v1.0/listFiles` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

