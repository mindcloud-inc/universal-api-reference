# Systeme.io: List Tags

Retrieves the collection of tags from Systeme.io.

```
GET https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-tags?${params}`, {
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
| `query` | string | no | Text search query. |
| `limit` | number | no | Cursor-based pagination limit (10-100). |
| `startingAfter` | number | no | Cursor-based pagination starting after this ID. |
| `order` | string | no | Cursor-based ordering: asc or desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Tag creation date-time. |
| `id` | number | Tag ID. |
| `name` | string | Tag name. |

## Native endpoint

Through the native Systeme.io API, this operation is `GET /api/tags` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

