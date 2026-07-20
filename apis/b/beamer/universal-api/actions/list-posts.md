# Beamer: List Posts

Retrieves posts from Beamer.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/list-posts?${params}`, {
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
| `filter` | string | no | Retrieve posts with a matching segmentation filter. |
| `forceFilter` | string | no | Only retrieve posts that match this segmentation filter. |
| `filterUrl` | string | no | Include posts with a matching segmentation URL. |
| `dateFrom` | string | no | Retrieve posts published after this ISO-8601 date. |
| `dateTo` | string | no | Retrieve posts published before this ISO-8601 date. |
| `language` | string | no | Retrieve posts with translations in this language. |
| `category` | string | no | Retrieve posts with this category. |
| `published` | boolean | no | Retrieve only published or draft posts. |
| `archived` | boolean | no | Retrieve only archived or non-archived posts. |
| `expired` | boolean | no | Retrieve only expired or non-expired posts. |
| `filterByUserId` | boolean | no | Retrieve posts filtered by user ID. |
| `userFirstName` | string | no | First name of the user viewing these posts. |
| `userLastName` | string | no | Last name of the user viewing these posts. |
| `userEmail` | string | no | Email of the user viewing these posts. |
| `userId` | string | no | ID of the user viewing these posts. |
| `traceableLinks` | boolean | no | Whether to include traceable links in posts. |
| `ignoreRequestDetails` | boolean | no | Ignore request details used for analytics. |
| `saveViews` | boolean | no | Whether to save views for the requesting user. |
| `ignoreFilters` | boolean | no | Ignore feed filters when retrieving posts. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `GET /v0/posts` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

