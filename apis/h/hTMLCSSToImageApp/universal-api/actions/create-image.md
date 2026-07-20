# HTML/CSS to Image app: Create Image



```
POST https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-image', {
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
| `html` | string | no | HTML markup to render into an image. |
| `css` | string | no | CSS styles to apply to the HTML or inject into the target URL page. |
| `url` | string | no | Public URL to screenshot instead of rendering HTML directly. |
| `googleFonts` | string | no | Google Fonts to load before rendering. |
| `deviceScale` | number | no | Pixel ratio for rendering, from 0.1 to 3. |
| `viewportWidth` | number | no | Viewport width in pixels. |
| `viewportHeight` | number | no | Viewport height in pixels. |
| `selector` | string | no | CSS selector for the element to capture. |
| `msDelay` | number | no | Milliseconds to wait before rendering. |
| `maxWaitMs` | number | no | Maximum wait time before capture. |
| `renderWhenReady` | boolean | no | Wait for ScreenshotReady() before capture. |
| `fullScreen` | boolean | no | Capture the full scrollable page height. |
| `blockConsentBanners` | boolean | no | Block consent and cookie banners before capture. |
| `colorScheme` | string | no | Render using light or dark mode. |
| `timezone` | string | no | IANA timezone to use while rendering. |
| `disableTwemoji` | boolean | no | Use native emoji fonts instead of Twemoji. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Generated image identifier. |
| `url` | string | Permanent URL for the generated image. |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `POST /v1/image` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

