# Instructure: Create Folder

Creates a new folder in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "parentFolderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "parentFolderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the new folder. |
| `parentFolderId` | string | yes | The Canvas parent folder ID. |

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

Through the native Instructure API, this operation is `POST /folders/:parent_folder_id/folders` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

