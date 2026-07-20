# Instructure: List Folder Files

Retrieves files in a folder from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-folder-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-folder-files?connectionId=$CONNECTION_ID&limit=25&offset=0&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-folder-files?${params}`, {
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
| `folderId` | string | yes | The Canvas folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "string",
      "displayName": "Ava Chen",
      "filename": "Ava Chen",
      "folderId": 1,
      "hidden": true,
      "id": 1,
      "locked": true,
      "size": 1,
      "thumbnailUrl": "https://example.com",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `createdAt` | string |  |
| `displayName` | string |  |
| `filename` | string |  |
| `folderId` | number |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `locked` | boolean |  |
| `size` | number |  |
| `thumbnailUrl` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /folders/:folder_id/files` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-folder-files.md) for the provider-specific parameters and requirements.

