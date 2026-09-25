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

```json
{
  "success": true,
  "data": [
    {
      "contents": [
        {}
      ],
      "errors": "string",
      "isPending": true,
      "isSitemapsIndex": true,
      "lastDownloaded": "string",
      "lastSubmitted": "string",
      "path": "string",
      "type": "string",
      "warnings": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contents` | array<object> | Per-content-type submission and indexing counts for the sitemap. |
| `errors` | string | Number of errors reported for the sitemap. |
| `isPending` | boolean | Whether the sitemap was submitted but processing has not finished. |
| `isSitemapsIndex` | boolean | Whether the sitemap is a sitemap index file. |
| `lastDownloaded` | string | Date and time Google last downloaded the sitemap. |
| `lastSubmitted` | string | Date and time the sitemap was last submitted, if any. |
| `path` | string | The URL of the sitemap. |
| `type` | string | The sitemap type reported by the provider. |
| `warnings` | string | Number of warnings reported for the sitemap. |

## Native endpoint

Through the native Google Search Console API, this operation is `GET sites/:siteUrl/sitemaps` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sitemaps.md) for the provider-specific parameters and requirements.

