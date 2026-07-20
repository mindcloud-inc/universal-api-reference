# Beamer: List Unread Posts

Retrieves unread posts from Beamer.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/list-unread-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/list-unread-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/list-unread-posts?${params}`, {
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
| `filter` | string | no |  |
| `forceFilter` | string | no |  |
| `filterUrl` | string | no |  |
| `dateFrom` | string | no |  |
| `language` | string | no |  |
| `category` | string | no |  |
| `userFirstName` | string | no |  |
| `userLastName` | string | no |  |
| `userEmail` | string | no |  |
| `userId` | string | no |  |
| `traceableLinks` | boolean | no |  |
| `ignoreRequestDetails` | boolean | no |  |
| `saveViews` | boolean | no |  |
| `markAsRead` | boolean | no |  |
| `ignoreFilters` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `GET /v0/unread` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-unread-posts.md) for the provider-specific parameters and requirements.

