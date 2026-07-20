# SCOTUSblog: List Cases in the Pipeline Posts



```
GET https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-cases-in-the-pipeline-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SCOTUSblog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-cases-in-the-pipeline-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCOTUSblog/latest/actions/list-cases-in-the-pipeline-posts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SCOTUSblog API returns.

## Native endpoint

Through the native SCOTUSblog API, this operation is `GET /category/cases-in-the-pipeline/feed/` (base URL `https://www.scotusblog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cases-in-the-pipeline-posts.md) for the provider-specific parameters and requirements.

