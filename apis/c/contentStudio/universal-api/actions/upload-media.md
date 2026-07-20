# ContentStudio: Upload Media

Creates a media asset in a ContentStudio workspace.

```
POST https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/upload-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/upload-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/upload-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no | Media file to upload. |
| `folder_id` | string | no | Folder ID to upload into. |
| `url` | string | no | Remote URL to import media from. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dimensions": {},
      "extension": "string",
      "folderId": "string",
      "Id": "string",
      "isProcessing": true,
      "mimeType": "string",
      "name": "Ava Chen",
      "size": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `dimensions` | object |  |
| `extension` | string |  |
| `folderId` | string |  |
| `Id` | string |  |
| `isProcessing` | boolean |  |
| `mimeType` | string |  |
| `name` | string |  |
| `size` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `POST /workspaces/:workspace_id/media` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media.md) for the provider-specific parameters and requirements.

