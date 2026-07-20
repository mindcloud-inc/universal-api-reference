# HTML/CSS to Image app: Create Template



```
POST https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | HTML markup to save in the template. |
| `css` | string | no | CSS styles for the template. |
| `name` | string | no | Short name for the template. |
| `description` | string | no | Optional description for the template. |
| `googleFonts` | string | no | Google Fonts to load before rendering the template. |
| `selector` | string | no | CSS selector for the element to capture. |
| `msDelay` | number | no | Milliseconds to wait before rendering. |
| `maxWaitMs` | number | no | Maximum wait time before capture. |
| `deviceScale` | number | no | Pixel ratio for rendering, from 0.1 to 3. |
| `renderWhenReady` | boolean | no | Wait for ScreenshotReady() before capture. |
| `viewportWidth` | number | no | Viewport width in pixels. |
| `viewportHeight` | number | no | Viewport height in pixels. |
| `colorScheme` | string | no | Render using light or dark mode. |
| `timezone` | string | no | IANA timezone to use while rendering. |
| `disableTwemoji` | boolean | no | Use native emoji fonts instead of Twemoji. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "templateId": "string",
      "templateVersion": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `templateId` | string |  |
| `templateVersion` | number |  |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `POST /v1/template` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

