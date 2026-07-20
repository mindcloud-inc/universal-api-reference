# DataForSEO: Get Organic Search Results

Retrieves organic search results from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-organic-search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-organic-search-results?connectionId=$CONNECTION_ID&search_engine=bing&keyword=string&language_code=string&location_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search_engine": "bing",
  "keyword": "string",
  "language_code": "string",
  "location_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-organic-search-results?${params}`, {
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
| `search_engine` | list<string> | yes | Search engine name. One of: `bing`, `google`, `yahoo`. |
| `keyword` | string | yes | Search keyword. |
| `language_code` | string | yes | Search engine language code. |
| `location_name` | string | yes | Full location name in hierarchical comma-separated format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device` | list<string> | no | Device type. One of: `desktop`, `mobile`. |
| `depth` | number | no | Number of results in the SERP. |
| `max_crawl_pages` | number | no | Number of search results pages to crawl. |
| `people_also_ask_click_depth` | number | no | Click depth on the people_also_ask element. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breadcrumb": "string",
      "description": "string",
      "domain": "string",
      "highlighted": [
        "string"
      ],
      "items": [
        "string"
      ],
      "links": [
        {}
      ],
      "page": 1,
      "rankAbsolute": 1,
      "rankGroup": 1,
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "websiteName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breadcrumb` | string | Displayed breadcrumb text when available. |
| `description` | string | Displayed snippet or description when available. |
| `domain` | string | Result domain when available. |
| `highlighted` | array<string> | Highlighted snippet fragments when available. |
| `items` | array | Nested SERP items for grouped result blocks. |
| `links` | array<object> | Additional sitelink-style links returned for some organic results. |
| `page` | number | SERP page number for the result block. |
| `rankAbsolute` | number | Absolute rank position in the page results. |
| `rankGroup` | number | Grouped rank position for the result block. |
| `title` | string | Primary title shown for the result block. |
| `type` | string | SERP result block type. |
| `url` | string | Result URL when the block links directly to a page. |
| `websiteName` | string | Displayed website or source name when available. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/serp/:search_engine/organic/live/advanced.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organic-search-results.md) for the provider-specific parameters and requirements.

