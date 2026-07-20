# Screenshotbase: Take Website Screenshot

Captures a website screenshot with Screenshotbase.

```
POST https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/take-website-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenshotbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/take-website-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/take-website-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The URL of the website you want to render. |
| `format` | string | no | The format of the image returned. Default: `png`. |
| `quality` | number | no | The quality of the image returned for JPG or JPEG output. Default: `80`. |
| `fullPage` | boolean | no | Take a screenshot of the full page. Default: `false`. |
| `viewportWidth` | number | no | The browser viewport width in pixels. Default: `1280`. |
| `viewportHeight` | number | no | The browser viewport height in pixels. Default: `800`. |
| `ipCountryCode` | string | no | ISO 3166-1 alpha-2 country code for the screenshot IP location. |
| `delay` | number | no | Seconds to wait before taking the screenshot. Default: `0`. |
| `timeout` | number | no | The timeout in seconds for the page load. Default: `60`. |
| `waitUntil` | string | no | When the screenshot should be taken based on page load state. Default: `load`. |
| `blockCookieBanners` | boolean | no | Block cookie banners on the page. Default: `false`. |
| `blockAds` | boolean | no | Block ads on the page. Default: `false`. |
| `blockChats` | boolean | no | Block chat widgets on the page. Default: `false`. |
| `hideSelectors[]` | array<string> | no | CSS selectors to hide before taking the screenshot. |
| `styles` | string | no | Custom CSS styles to inject before taking the screenshot. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Screenshotbase API returns.

## Native endpoint

Through the native Screenshotbase API, this operation is `GET /take` (base URL `https://api.screenshotbase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/take-website-screenshot.md) for the provider-specific parameters and requirements.

