# Teamhood: Query Items

Finds items in Teamhood by query filters.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/query-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/query-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/query-items?${params}`, {
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
| `assignedUserId` | string | no | Filter items by assignee. |
| `boardId` | string | no | Filter items by board. |
| `completed` | string | no | Filter completed items. |
| `completedSince` | string | no | Filter items completed since the given ISO timestamp. |
| `createdSince` | string | no | Filter items created since the given ISO timestamp. |
| `includeChildItems` | string | no | Include child items in the response. |
| `modifiedSince` | string | no | Filter items modified since the given ISO timestamp. |
| `ownerId` | string | no | Filter items by owner. |
| `parentId` | string | no | Filter child items by parent item. |
| `rowId` | string | no | Filter items by row. |
| `skip` | string | no | Number of items to skip. |
| `statusId` | string | no | Filter items by status. |
| `take` | string | no | Number of items to return. |
| `workspaceId` | string | no | Filter items by workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "nextPageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Teamhood items matching the requested query filters. |
| `nextPageUrl` | string | The next page URL when additional items are available. |

## Native endpoint

Through the native Teamhood API, this operation is `GET /items` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-items.md) for the provider-specific parameters and requirements.

