# Mural: List Murals for Room

Finds murals in Mural for a room.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-murals-for-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-murals-for-room?connectionId=$CONNECTION_ID&limit=25&offset=0&roomId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "roomId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-murals-for-room?${params}`, {
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
| `muralsFolder` | string | no | Filter murals by their corresponding folder. |
| `muralsSortBy` | string | no | Sort murals by the documented Mural sort order. |
| `muralsStatus` | string | no | Filter murals by active or archived status. |
| `roomId` | number | yes | Unique identifier of a room. |

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

Through the native Mural API, this operation is `GET /rooms/:roomId/murals` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-murals-for-room.md) for the provider-specific parameters and requirements.

