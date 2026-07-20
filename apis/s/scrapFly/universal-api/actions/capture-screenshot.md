# ScrapFly: Capture Screenshot

Retrieves a webpage screenshot from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/capture-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/capture-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fweb-scraping.dev%2Fproduct%2F1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://web-scraping.dev/product/1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/capture-screenshot?${params}`, {
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
| `capture` | string | no | Area to capture: viewport, full page, or a CSS selector/XPath target. Example: `fullpage`. |
| `format` | string | no | Image format for the returned screenshot, such as jpeg or png. Example: `jpeg`. |
| `resolution` | string | no | Screen resolution in WIDTHxHEIGHT format. Example: `1920x1080`. |
| `url` | string | yes | Target URL to capture as a screenshot. Example: `https://web-scraping.dev/product/1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `GET /screenshot` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-screenshot.md) for the provider-specific parameters and requirements.

