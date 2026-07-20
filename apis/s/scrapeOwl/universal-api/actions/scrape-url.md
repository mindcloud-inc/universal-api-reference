# ScrapeOwl: Scrape URL



```
GET https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/scrape-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/scrape-url?${params}`, {
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
| `url` | string | yes | Target URL to scrape. Example: `https://example.com`. |
| `elements[]` | array<object> | no | List of element selectors to extract from the webpage. Example: `[object Object]`. |
| `html` | boolean | no | Return the page HTML when true. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jsonResponse` | boolean | no | Return JSON formatted output when true. Default: `true`. |
| `returnHeaders` | boolean | no | Return headers from the target website server. Default: `false`. |
| `returnCookies` | boolean | no | Return cookies from the target website server. Default: `false`. |
| `headers` | object | no | HTTP headers to send to the target URL. Example: `[object Object]`. |
| `cookies` | string | no | Cookie header value to send to the target URL. |
| `requestMethod` | string | no | Target request method: GET, POST, or PUT. Default: `GET`. Example: `GET`. |
| `postData` | string | no | Data to send when requestMethod is POST or PUT. Example: `name=value`. |
| `renderJs` | boolean | no | Use a headless Chrome instance to execute JavaScript. Default: `false`. |
| `waitFor` | string | no | Element selector or millisecond duration to wait before scraping. Example: `p`. |
| `customJs` | string | no | JavaScript to run on the page before extraction. Example: `window.scrollTo(0,document.body.scrollHeight);`. |
| `screenshot` | boolean | no | Capture a screenshot; only works with render_js. Default: `false`. |
| `blockResources` | boolean | no | Block CSS, images, and fonts while rendering JavaScript. Default: `true`. |
| `rejectRequests[]` | array<string> | no | Resource extensions or URLs to block during render_js scraping. Example: `css,png,jpg`. |
| `premiumProxies` | boolean | no | Use residential premium proxies. Default: `false`. |
| `country` | string | no | Residential proxy source country ISO code. Example: `us`. |
| `session` | string | no | Sticky session value for reusing the same IP address. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cookies": [
        {}
      ],
      "credits": {
        "available": 1,
        "request_cost": 1,
        "used": 1
      },
      "data": {},
      "html": "string",
      "is_billed": true,
      "resolved_url": "https://example.com",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cookies` | array<object> | Cookies returned by the scrape request. |
| `credits` | object | Credit balance and request cost details. |
| `credits.available` | number | Available credits. |
| `credits.request_cost` | number | Credits charged for this request. |
| `credits.used` | number | Used credits. |
| `data` | object | Extracted element results when elements are requested. |
| `html` | string | Returned page HTML or raw response content. |
| `is_billed` | boolean | Whether the request was billed. |
| `resolved_url` | string | Final resolved URL after redirects. |
| `status` | number | ScrapeOwl response status code. |

## Native endpoint

Through the native ScrapeOwl API, this operation is `POST /scrape` (base URL `https://api.scrapeowl.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url.md) for the provider-specific parameters and requirements.

