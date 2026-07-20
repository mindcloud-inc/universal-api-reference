# Advanced Scraper: Scrape URL

Retrieves scraped data from a remote URL in Advanced Scraper.

```
GET https://connect.mindcloud.co/v1/universal/advancedScraper/latest/actions/scrape-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Advanced Scraper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advancedScraper/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advancedScraper/latest/actions/scrape-url?${params}`, {
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
| `url` | string | yes | Remote URL to scrape. |
| `country` | string | no | Optional two-character country code for originating IP address. |
| `render` | boolean | no | Render the remote page with a browser. Set false for images, JSON, PDFs, XML, or other files. |
| `selector` | string | no | CSS selector to return only selected content. |
| `timeout` | number | no | Timeout in seconds before returning a result. APILayer documents min 5 and max 45. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "options": {},
      "request_headers": {},
      "response_headers": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | The scraped response body returned by APILayer. |
| `options` | object | Scraping options applied by APILayer for the request. |
| `request_headers` | object | Headers APILayer sent to the remote site. |
| `response_headers` | object | Headers returned by the remote site. |
| `url` | string | The remote URL that was scraped. |

## Native endpoint

Through the native Advanced Scraper API, this operation is `GET /scraper` (base URL `https://api.apilayer.com/adv_scraper`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url.md) for the provider-specific parameters and requirements.

