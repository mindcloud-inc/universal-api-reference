# SCOTUSblog: List Posts by Author



```
GET https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-posts-by-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SCOTUSblog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-posts-by-author?connectionId=$CONNECTION_ID&authorSlug=adam-feldman" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorSlug": "adam-feldman"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-posts-by-author?${params}`, {
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
| `authorSlug` | string | yes | Author archive slug from the SCOTUSblog URL, for example adam-feldman. Example: `adam-feldman`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SCOTUSblog API returns.

## Native endpoint

Through the native SCOTUSblog API, this operation is `GET /author/:authorSlug/feed/` (base URL `https://www.scotusblog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts-by-author.md) for the provider-specific parameters and requirements.

