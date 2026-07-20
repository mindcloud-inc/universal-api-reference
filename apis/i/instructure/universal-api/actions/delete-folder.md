# Instructure: Delete Folder

Deletes a folder from Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-folder?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-folder?${params}`, {
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

Through the native Instructure API, this operation is `DELETE /folders/:folder_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

