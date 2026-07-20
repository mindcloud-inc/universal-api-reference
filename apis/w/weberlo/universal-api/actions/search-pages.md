# Weberlo: Search Pages

Finds pages in Weberlo by search query.

```
GET https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/search-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/search-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&search=landing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "landing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/search-pages?${params}`, {
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
| `search` | string | yes | Search term for matching pages. Example: `landing`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weberlo API returns.

## Native endpoint

Through the native Weberlo API, this operation is `GET /page/search` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-pages.md) for the provider-specific parameters and requirements.

