# Frame.io v4: Copy Version Stack

Copies a version stack in Frame.io v4.

```
POST https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/copy-version-stack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/copy-version-stack" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "versionStackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/copy-version-stack', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "versionStackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `versionStackId` | string | yes |  |
| `copyMetadata` | boolean | no |  |
| `data` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "headVersion": {
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
      },
      "id": "string",
      "name": "Ava Chen",
      "parentId": "string",
      "projectId": "string",
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
| `headVersion` | object |  |
| `headVersion.createdAt` | date | Creation timestamp |
| `headVersion.fileSize` | number | File size in bytes |
| `headVersion.id` | string | File, Folder, or Version Stack ID |
| `headVersion.mediaType` | string | File media type |
| `headVersion.name` | string | File or folder Name |
| `headVersion.parentId` | string | Parent Folder or Version Stack ID |
| `headVersion.projectId` | string | Project ID |
| `headVersion.status` | string |  |
| `headVersion.type` | string |  |
| `headVersion.updatedAt` | date | Update timestamp |
| `headVersion.viewUrl` | string | URL to view the asset in the Frame.io web application |
| `id` | string | File, Folder, or Version Stack ID |
| `name` | string | File or folder Name |
| `parentId` | string | Parent Folder or Version Stack ID |
| `projectId` | string | Project ID |
| `type` | string |  |
| `updatedAt` | date | Update timestamp |
| `viewUrl` | string | URL to view the asset in the Frame.io web application |

## Native endpoint

Through the native Frame.io v4 API, this operation is `POST /accounts/:accountId/version_stacks/:versionStackId/copy` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-version-stack.md) for the provider-specific parameters and requirements.

