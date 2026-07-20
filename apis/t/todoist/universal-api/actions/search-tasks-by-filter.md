# Todoist: Search Tasks By Filter

Finds tasks in Todoist by filter query.

```
GET https://connect.mindcloud.co/v1/universal/todoist/latest/actions/search-tasks-by-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/search-tasks-by-filter?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/todoist/latest/actions/search-tasks-by-filter?${params}`, {
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
| `query` | string | yes | Filter query string |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextCursor": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextCursor` | string | Cursor for the next page when available |
| `results` | array<object> | Tasks matching the filter query |

## Native endpoint

Through the native Todoist API, this operation is `GET /api/v1/tasks/filter` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks-by-filter.md) for the provider-specific parameters and requirements.

