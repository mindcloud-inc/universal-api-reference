# Urlbox: Create Asynchronous Render

Creates an asynchronous render in Urlbox.

```
POST https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-asynchronous-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Urlbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-asynchronous-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-asynchronous-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | The URL to render Example: `https://example.com`. |
| `html` | string | no | The HTML to render Example: `<html><body>Hello</body></html>`. |
| `format` | string | no | The output format of the render Example: `png`. |
| `width` | number | no | The viewport width in pixels Example: `1280`. |
| `height` | number | no | The viewport height in pixels Example: `720`. |
| `fullPage` | boolean | no | Capture the full scrollable page |
| `selector` | string | no | Capture only the matching element selector Example: `#main`. |
| `hideCookieBanners` | boolean | no | Automatically hide cookie banners |
| `clickAccept` | boolean | no | Try to click the cookie accept button |
| `blockAds` | boolean | no | Block popular advertising networks |

## Response

```json
{
  "success": true,
  "data": [
    {
      "renderId": "string",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `renderId` | string | Identifier for the accepted async render request. |
| `status` | string | Accepted render status, typically created. |
| `statusUrl` | string | Polling URL for checking the current render status. |

## Native endpoint

Through the native Urlbox API, this operation is `POST /v1/render/async` (base URL `https://api.urlbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asynchronous-render.md) for the provider-specific parameters and requirements.

