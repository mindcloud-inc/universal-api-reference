# Linkbreakers: List Directories

Retrieves a list of directories from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-directories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-directories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-directories?${params}`, {
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
| `parentDirectoryId` | string | no | Filter directories by parent directory ID. |
| `search` | string | no | Search query to filter directories by name. |
| `includeRoot` | boolean | no | Also include root-level directories when filtering by parent. |
| `recursive` | boolean | no | Return directories recursively. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directories": [
        {
          "createdAt": "string",
          "id": "string",
          "name": "Ava Chen",
          "parentDirectoryId": "string",
          "path": "string",
          "updatedAt": "string",
          "workspaceId": "string"
        }
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directories` | array<object> | Directories matching the current filter. |
| `directories[].createdAt` | string |  |
| `directories[].id` | string |  |
| `directories[].name` | string |  |
| `directories[].parentDirectoryId` | string |  |
| `directories[].path` | string |  |
| `directories[].updatedAt` | string |  |
| `directories[].workspaceId` | string |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/directories` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-directories.md) for the provider-specific parameters and requirements.

