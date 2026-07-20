# Quick Scraper: Parse URL

Retrieves scraped page content from Quick Scraper.

```
GET https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/parse-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quick Scraper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/parse-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/parse-url?${params}`, {
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
| `url` | string | yes | The public page URL Quick Scraper should fetch and return. Default: `https://example.com`. Example: `https://example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quick Scraper API returns.

## Native endpoint

Through the native Quick Scraper API, this operation is `GET /parse` (base URL `https://api.quickscraper.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-url.md) for the provider-specific parameters and requirements.

