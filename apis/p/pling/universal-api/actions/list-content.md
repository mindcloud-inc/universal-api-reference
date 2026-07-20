# Pling: List Content

Retrieves public content listings from Pling.

```
GET https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pling `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortmode` | string | no | Pling sort mode such as new or high. One of: `0`, `1`, `2`, `3`. Default: `new`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changed": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "detailpage": "string",
      "downloads": 1,
      "id": "string",
      "name": "Ava Chen",
      "personid": "string",
      "score": 1,
      "summary": "string",
      "typename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changed` | date | Last update timestamp. |
| `created` | date | Creation timestamp. |
| `detailpage` | string | Pling detail page URL. |
| `downloads` | number | Download count. |
| `id` | string | Content identifier. |
| `name` | string | Content title. |
| `personid` | string | Publishing username. |
| `score` | number | Provider score. |
| `summary` | string | Short content summary. |
| `typename` | string | Content type display name. |

## Native endpoint

Through the native Pling API, this operation is `GET /content/data` (base URL `https://api.pling.com/ocs/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-content.md) for the provider-specific parameters and requirements.

