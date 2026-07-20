# Mural: List Recently Opened Murals for Workspace

Finds recently opened murals in Mural for a workspace.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-recently-opened-murals-for-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-recently-opened-murals-for-workspace?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-recently-opened-murals-for-workspace?${params}`, {
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
| `workspaceId` | string | yes | Unique identifier of a workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_canvasLink": "https://example.com",
      "createdBy": {},
      "createdOn": 1,
      "favorite": true,
      "folderId": "string",
      "id": "string",
      "infinite": true,
      "roomId": 1,
      "sharingSettings": {},
      "state": "string",
      "status": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "updatedBy": {},
      "updatedOn": 1,
      "visitorsSettings": {},
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_canvasLink` | string |  |
| `createdBy` | object |  |
| `createdOn` | number |  |
| `favorite` | boolean |  |
| `folderId` | string |  |
| `id` | string |  |
| `infinite` | boolean |  |
| `roomId` | number |  |
| `sharingSettings` | object |  |
| `state` | string |  |
| `status` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `updatedBy` | object |  |
| `updatedOn` | number |  |
| `visitorsSettings` | object |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /workspaces/:workspaceId/murals/recent` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-recently-opened-murals-for-workspace.md) for the provider-specific parameters and requirements.

