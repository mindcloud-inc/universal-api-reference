# Frame.io v4: Update File

Updates an existing file in Frame.io v4.

```
PUT https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "fileId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/update-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "fileId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `fileId` | string | yes |  |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileSize": 1,
      "id": "string",
      "mediaType": "string",
      "name": "Ava Chen",
      "parentId": "string",
      "projectId": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `fileSize` | number | File size in bytes |
| `id` | string | File, Folder, or Version Stack ID |
| `mediaType` | string | File media type |
| `name` | string | File or folder Name |
| `parentId` | string | Parent Folder or Version Stack ID |
| `projectId` | string | Project ID |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date | Update timestamp |
| `viewUrl` | string | URL to view the asset in the Frame.io web application |

## Native endpoint

Through the native Frame.io v4 API, this operation is `PATCH /accounts/:accountId/files/:fileId` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file.md) for the provider-specific parameters and requirements.

