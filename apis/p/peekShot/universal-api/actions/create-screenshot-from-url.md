# PeekShot: Create Screenshot from URL

Creates a screenshot from a URL in PeekShot.

```
POST https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeekShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Unique project identifier. |
| `url` | string | yes | Website URL to capture. |
| `width` | string | no | Screenshot width. Docs default: 1280. |
| `height` | string | no | Screenshot height. Docs default: 1024. |
| `injectCss` | string | no | Custom CSS to apply before capture. |
| `injectJs` | string | no | Custom JavaScript to apply before capture. |
| `fileType` | string | no | Output format: jpeg, png, webp, or avif. |
| `retina` | string | no | Use true for higher-resolution screenshots. |
| `delay` | string | no | Delay in seconds before capture. Allowed range: 0 to 60. |
| `fullPage` | string | no | Capture the full page instead of only the viewport. |
| `disableJavascript` | string | no | Disable page JavaScript during rendering. |
| `emulateDevice` | string | no | Render the page using a supported device profile. |
| `disableAnimations` | string | no | Disable animations before capture. |
| `proxyUrl` | string | no | HTTP proxy URL, including authentication if needed. |
| `customHeader` | string | no | Inject a custom header into the page request. |
| `elementSelector` | string | no | Target one element with a CSS selector or an xpath= expression. |
| `blockCookieBanner` | string | no | Hide cookie banners. Docs default: true. |
| `blockAds` | string | no | Block ads. Docs default: true. |
| `blockPopupsByHeuristics` | string | no | Block popups heuristically. Docs default: false. |
| `cookieTemplateId` | string | no | Cookie template identifier to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "creditRequired": 1,
        "organizationId": 1,
        "requestId": 1
      },
      "message": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.creditRequired` | number | Credits required for the request. |
| `data.organizationId` | number | Organization ID returned by PeekShot. |
| `data.requestId` | number | Created screenshot request ID. |
| `message` | string | Provider message. |
| `status` | string | Request status. |
| `statusCode` | number | HTTP-style status code returned by the provider. |

## Native endpoint

Through the native PeekShot API, this operation is `POST /screenshots` (base URL `https://api.peekshot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-screenshot-from-url.md) for the provider-specific parameters and requirements.

