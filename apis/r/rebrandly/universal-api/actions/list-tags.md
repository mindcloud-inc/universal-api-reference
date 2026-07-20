# Rebrandly: List Tags

Retrieves tags from Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-tags?${params}`, {
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
| `limit` | number | no | Maximum number of tags to return. Example: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Field used to sort the tags collection. Example: `name`. |
| `orderDir` | string | no | Sort direction for the tags collection. Example: `asc`. |
| `last` | string | no | Cursor: the last tag ID returned by the previous page. Example: `cfa87d9986144793b8608026ef7aa50e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "clicks": 1,
      "color": "string",
      "id": "string",
      "name": "Ava Chen",
      "scans": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `clicks` | number |  |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scans` | object |  |

## Native endpoint

Through the native Rebrandly API, this operation is `GET /tags` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

