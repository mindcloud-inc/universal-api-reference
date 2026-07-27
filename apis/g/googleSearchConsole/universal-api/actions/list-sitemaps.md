# Google Search Console: List Sitemaps



```
GET https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/list-sitemaps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/list-sitemaps?connectionId=$CONNECTION_ID&siteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/list-sitemaps?${params}`, {
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
| `siteUrl` | list<string> | yes | The Search Console property URL whose submitted sitemaps you want to list. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sitemapIndex` | string | no | Optional sitemap index URL to limit the results to the entries included in that sitemap index. Example: `https://www.example.com/sitemap-index.xml`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `GET sites/:siteUrl/sitemaps` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sitemaps.md) for the provider-specific parameters and requirements.

