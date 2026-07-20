# ScrapeOps: Search Walmart Products

Retrieves Walmart search results from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-walmart-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-walmart-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-walmart-products?${params}`, {
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
| `country` | string | no | The 2-letter country code to scrape Walmart search results from. |
| `query` | string | no | Walmart search query. |
| `tld` | string | no | The Walmart top-level domain to scrape, such as com or ca. |
| `url` | string | no | Full Walmart search URL to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeOps API returns.

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/walmart/search` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-walmart-products.md) for the provider-specific parameters and requirements.

