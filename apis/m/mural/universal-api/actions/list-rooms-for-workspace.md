# Mural: List Rooms for Workspace

Finds rooms in Mural for a workspace.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-rooms-for-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-rooms-for-workspace?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-rooms-for-workspace?${params}`, {
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
      "confidential": true,
      "createdBy": {},
      "createdOn": 1,
      "description": "string",
      "favorite": true,
      "id": 1,
      "isMember": true,
      "name": "Ava Chen",
      "type": "string",
      "updatedBy": {},
      "updatedOn": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidential` | boolean |  |
| `createdBy` | object |  |
| `createdOn` | number |  |
| `description` | string |  |
| `favorite` | boolean |  |
| `id` | number |  |
| `isMember` | boolean |  |
| `name` | string |  |
| `type` | string |  |
| `updatedBy` | object |  |
| `updatedOn` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /workspaces/:workspaceId/rooms` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rooms-for-workspace.md) for the provider-specific parameters and requirements.

