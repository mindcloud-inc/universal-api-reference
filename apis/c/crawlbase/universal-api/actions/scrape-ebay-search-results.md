# Crawlbase: Scrape Ebay Search Results

Retrieves eBay search results from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/scrape-ebay-search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/scrape-ebay-search-results?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.ebay.com%2Fsch%2Fi.html%3F_nkw%3Diphone%2Bx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.ebay.com/sch/i.html?_nkw=iphone+x"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/scrape-ebay-search-results?${params}`, {
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
| `url` | string | yes | URL to scrape with the ebay-serp Crawlbase data scraper. Example: `https://www.ebay.com/sch/i.html?_nkw=iphone+x`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {},
      "original_status": 1,
      "pc_status": 1,
      "remaining_requests": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | object |  |
| `original_status` | number |  |
| `pc_status` | number |  |
| `remaining_requests` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-ebay-search-results.md) for the provider-specific parameters and requirements.

