# Botsonic: List Bots

Retrieves all bots in Botsonic.

```
GET https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-bots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-bots?${params}`, {
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
| `searchQuery` | string | no | Optional bot search query. Example: `support`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Bot field to sort by. Example: `created_at`. |
| `sortOrder` | string | no | Sort direction. Example: `desc`. |
| `workspaceId` | string | no | Optional workspace identifier. Example: `workspace_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "page": 1,
      "pages": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Bot records. |
| `page` | number | Current page. |
| `pages` | number | Total pages. |
| `size` | number | Page size. |
| `total` | number | Total bots. |

## Native endpoint

Through the native Botsonic API, this operation is `GET /v1/business/bot/all` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bots.md) for the provider-specific parameters and requirements.

