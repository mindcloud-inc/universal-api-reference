# Google Search Console: Delete Sitemap



```
DELETE https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/delete-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/delete-sitemap?connectionId=$CONNECTION_ID&siteUrl=https%3A%2F%2Fexample.com&feedpath=https%3A%2F%2Fwww.example.com%2Fsitemap.xml" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteUrl": "https://example.com",
  "feedpath": "https://www.example.com/sitemap.xml"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/delete-sitemap?${params}`, {
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
| `siteUrl` | list<string> | yes | The Search Console property URL that owns the sitemap. |
| `feedpath` | string | yes | The full URL of the sitemap to delete, for example https://www.example.com/sitemap.xml. Example: `https://www.example.com/sitemap.xml`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `DELETE sites/:siteUrl/sitemaps/:feedpath` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sitemap.md) for the provider-specific parameters and requirements.

