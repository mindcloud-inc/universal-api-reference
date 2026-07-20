# Frame.io v4: Create File Local Upload

Creates a new file via local upload in Frame.io v4.

```
POST https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-file-local-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-file-local-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "folderId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/create-file-local-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "folderId": "string",
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
| `folderId` | string | yes |  |
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
      "uploadUrls": [
        [
          {}
        ]
      ],
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
| `uploadUrls[]` | array<object> | File upload URLs. Number of URLs returned will vary depending on the file size. |
| `uploadUrls[].size` | number | Upload chunk size |
| `uploadUrls[].url` | string | S3 presigned URL. Client should make a PUT request to this URL that includes the "x-amz-acl: private" header along with the file or file chunk data. |
| `viewUrl` | string | URL to view the asset in the Frame.io web application |

## Native endpoint

Through the native Frame.io v4 API, this operation is `POST /accounts/:accountId/folders/:folderId/files/local_upload` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-local-upload.md) for the provider-specific parameters and requirements.

