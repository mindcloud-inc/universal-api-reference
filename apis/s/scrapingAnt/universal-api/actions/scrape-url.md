# ScrapingAnt: Scrape URL

Retrieves scraped page HTML from ScrapingAnt.

```
GET https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingAnt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url?${params}`, {
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
| `url` | string | yes | Fully qualified URL to scrape. Example: `https://example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browser` | boolean | no | Enable ScrapingAnt headless browser rendering. Default is true. |
| `timeout` | number | no | Maximum request runtime in seconds. ScrapingAnt supports 5-60 seconds. Example: `30`. |
| `returnPageSource` | boolean | no | Return server response data unaltered by browser rendering. Works only with browser=true. |
| `proxyType` | list<string> | no | Proxy pool type. Supported values are datacenter and residential. One of: `datacenter`, `residential`. |
| `proxyCountry` | string | no | Two-letter proxy country code, such as US, GB, BR, or DE. Example: `US`. |
| `cookies` | string | no | Cookie header string to pass to the target site. Example: `session_id=abc123; theme=light`. |
| `jsSnippet` | string | no | Base64-encoded JavaScript snippet to run after the page loads. Requires browser=true. |
| `waitForSelector` | string | no | CSS selector ScrapingAnt should wait for before returning the result. Requires browser=true. Example: `.content`. |
| `blockResource` | list<string> | no | Resource type to block while rendering, such as image, stylesheet, script, xhr, or fetch. One of: `document`, `eventsource`, `fetch`, `font`, `image`, `manifest`, `media`, `other`, `script`, `stylesheet`, `texttrack`, `websocket`, `xhr`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Scraped page HTML returned by ScrapingAnt. |

## Native endpoint

Through the native ScrapingAnt API, this operation is `GET /general` (base URL `https://api.scrapingant.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url.md) for the provider-specific parameters and requirements.

