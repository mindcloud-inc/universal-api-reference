# CINCEL: List Folders



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-folders?connectionId=$CONNECTION_ID&limit=25&offset=0&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-folders?${params}`, {
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
| `team` | string | yes | UUID of the team whose folders should be listed. |
| `includeDeleted` | boolean | no | Include deleted folders when true. |
| `nameLike` | string | no | Filter folders by partial name match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "team": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Folder creation timestamp. |
| `deletedAt` | date | Deletion timestamp when the folder has been deleted. |
| `name` | string | Folder name. |
| `team` | string | Owning team UUID. |
| `updatedAt` | date | Folder last update timestamp. |
| `uuid` | string | Folder UUID. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/folders` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

