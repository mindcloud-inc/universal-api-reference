# Langbase: Crawl Web Pages



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/crawl-web-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/crawl-web-pages?connectionId=$CONNECTION_ID&crawlKey=string&url%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlKey": "string",
  "url[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/crawl-web-pages?${params}`, {
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
| `crawlKey` | string | yes | Langbase crawl key for the `LB-CRAWL-KEY` request header. |
| `url[]` | array<string> | yes | Array of URLs to crawl. |
| `service` | list | no | Crawler service to use. One of: `0`, `1`. |
| `maxPages` | number | no | Maximum number of pages to crawl. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `POST v1/tools/crawl` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crawl-web-pages.md) for the provider-specific parameters and requirements.

