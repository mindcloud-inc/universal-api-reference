# Linkly: List Links

Retrieves links from Linkly.

```
GET https://connect.mindcloud.co/v1/universal/linkly/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/list-links?${params}`, {
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
| `search` | string | no | Search query to filter links. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        {}
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalEntries": 1,
      "totalPages": 1,
      "totalRows": 1,
      "workspaceLinkCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | array<object> | Links returned for the current page. |
| `pageNumber` | number | Current page number. |
| `pageSize` | number | Number of rows requested per page. |
| `totalEntries` | number | Total matching entries. |
| `totalPages` | number | Total number of pages. |
| `totalRows` | number | Total rows in the response set. |
| `workspaceLinkCount` | number | Total link count for the workspace. |

## Native endpoint

Through the native Linkly API, this operation is `GET /workspace/:workspace_id/list_links` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

