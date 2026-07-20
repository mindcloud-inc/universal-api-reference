# ScrapeOps: Search Ebay Listings

Retrieves eBay search results from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-ebay-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-ebay-listings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-ebay-listings?${params}`, {
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
| `query` | string | no | eBay search query. |
| `url` | string | no | Full eBay search URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "related_searches": [
        {
          "link": [
            "https://example.com"
          ],
          "query": [
            "string"
          ]
        }
      ],
      "search_information": {
        "query": "string",
        "total_count": 1,
        "total_count_displayed": "string"
      },
      "search_pagination": [
        {
          "current": [
            true
          ],
          "number": [
            1
          ],
          "url": [
            "https://example.com"
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `related_searches[].link` | array<string> | Related search links. |
| `related_searches[].query` | array<string> | Related search queries. |
| `search_information.query` | string | Search query. |
| `search_information.total_count` | number | Total count. |
| `search_information.total_count_displayed` | string | Displayed total count. |
| `search_pagination[].current` | array<boolean> | Current-page flags. |
| `search_pagination[].number` | array<number> | Pagination numbers. |
| `search_pagination[].url` | array<string> | Pagination URLs. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/ebay/search` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-ebay-listings.md) for the provider-specific parameters and requirements.

