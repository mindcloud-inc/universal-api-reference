# GoSquared: Search People

Finds people in GoSquared by search query.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/search-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/search-people?${params}`, {
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
| `query` | string | no | The search term to match against People records. |
| `fields` | string | no | A comma-delimited list of fields to include in each result row. Default: `id,email,name,last_seen`. |
| `presenter` | string | no | Modifies the response data structure. Default: `plain`. |
| `dateFormat` | string | no | Moment-compatible format for returned date values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "Links": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Primary email for the person. |
| `id` | string | GoSquared person identifier. |
| `Links` | array<object> | Provider link metadata returned for related person resources. |
| `name` | string | Display name for the person. |

## Native endpoint

Through the native GoSquared API, this operation is `GET people/v1/people` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

