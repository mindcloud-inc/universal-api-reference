# Instructure: List User Folders

Retrieves user folders from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-user-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-user-folders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-user-folders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allUrl": "https://example.com",
      "canUpload": true,
      "contextId": 1,
      "contextType": "string",
      "createdAt": "string",
      "filesCount": 1,
      "filesUrl": "https://example.com",
      "foldersCount": 1,
      "foldersUrl": "https://example.com",
      "forSubmissions": true,
      "fullName": "Ava Chen",
      "hiddenForUser": true,
      "id": 1,
      "locked": true,
      "lockedForUser": true,
      "name": "Ava Chen",
      "parentFolderId": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allUrl` | string |  |
| `canUpload` | boolean |  |
| `contextId` | number |  |
| `contextType` | string |  |
| `createdAt` | string |  |
| `filesCount` | number |  |
| `filesUrl` | string |  |
| `foldersCount` | number |  |
| `foldersUrl` | string |  |
| `forSubmissions` | boolean |  |
| `fullName` | string |  |
| `hiddenForUser` | boolean |  |
| `id` | number |  |
| `locked` | boolean |  |
| `lockedForUser` | boolean |  |
| `name` | string |  |
| `parentFolderId` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self/folders` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-folders.md) for the provider-specific parameters and requirements.

