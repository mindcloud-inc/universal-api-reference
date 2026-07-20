# Seven: List Groups

Retrieves groups from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=1&offset=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "1",
  "offset": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-groups?${params}`, {
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
| `limit` | number | yes | Limit the number of groups returned. |
| `offset` | number | yes | The starting point from which the list should be displayed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "members_count": 1,
        "name": "Ava Chen"
      },
      "pagingMetadata": {
        "count": 1,
        "has_more": true,
        "limit": 1,
        "offset": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.created` | date |  |
| `data.id` | number |  |
| `data.members_count` | number |  |
| `data.name` | string |  |
| `pagingMetadata` | object |  |
| `pagingMetadata.count` | number |  |
| `pagingMetadata.has_more` | boolean |  |
| `pagingMetadata.limit` | number |  |
| `pagingMetadata.offset` | number |  |
| `pagingMetadata.total` | number |  |

## Native endpoint

Through the native Seven API, this operation is `GET /groups` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

