# SCOTUSblog: List Posts by Category



```
GET https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-posts-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SCOTUSblog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-posts-by-category?connectionId=$CONNECTION_ID&categorySlug=court-news" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categorySlug": "court-news"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-posts-by-category?${params}`, {
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
| `categorySlug` | string | yes | Category archive slug from the SCOTUSblog URL, for example court-news. Example: `court-news`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SCOTUSblog API returns.

## Native endpoint

Through the native SCOTUSblog API, this operation is `GET /category/:categorySlug/feed/` (base URL `https://www.scotusblog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts-by-category.md) for the provider-specific parameters and requirements.

