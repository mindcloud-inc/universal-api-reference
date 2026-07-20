# ScrapingAnt: Scrape URL With Extended JSON

Retrieves extended JSON page data from ScrapingAnt.

```
GET https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-extended-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingAnt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-extended-json?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-extended-json?${params}`, {
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
| `url` | string | yes | Fully qualified URL to scrape with extended JSON output. Example: `https://example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browser` | boolean | no | Enable ScrapingAnt headless browser rendering. Default is true. |
| `timeout` | number | no | Maximum request runtime in seconds. ScrapingAnt supports 5-60 seconds. Example: `30`. |
| `returnPageSource` | boolean | no | Return server response data unaltered by browser rendering. Works only with browser=true. |
| `proxyType` | list<string> | no | Proxy pool type. Supported values are datacenter and residential. One of: `datacenter`, `residential`. |
| `proxyCountry` | string | no | Two-letter proxy country code, such as US, GB, BR, or DE. Example: `US`. |
| `waitForSelector` | string | no | CSS selector ScrapingAnt should wait for before returning the result. Requires browser=true. Example: `.content`. |
| `blockResource` | list<string> | no | Resource type to block while rendering, such as image, stylesheet, script, xhr, or fetch. One of: `document`, `eventsource`, `fetch`, `font`, `image`, `manifest`, `media`, `other`, `script`, `stylesheet`, `texttrack`, `websocket`, `xhr`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cookies": "string",
      "headers": [
        {}
      ],
      "html": "string",
      "iframes": [
        {}
      ],
      "statusCode": 1,
      "text": "string",
      "xhrs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cookies` | string | Response cookies from the scraped web page. |
| `headers` | array<object> | Response headers from the scraped page. |
| `html` | string | Content from the scraped web page. |
| `iframes` | array<object> | Iframe content captured from the scraped page. |
| `statusCode` | number | HTTP status code received from the scraped page. |
| `text` | string | Text content from the scraped web page. |
| `xhrs` | array<object> | XHR and fetch requests captured during browser-rendered scraping. |

## Native endpoint

Through the native ScrapingAnt API, this operation is `GET /extended` (base URL `https://api.scrapingant.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url-with-extended-json.md) for the provider-specific parameters and requirements.

