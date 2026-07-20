# ScreenshotAPI: Render Custom HTML

Creates a screenshot from custom HTML in ScreenshotAPI.

```
POST https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/render-custom-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/render-custom-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customHtml": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/render-custom-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customHtml": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customHtml` | string | yes | HTML markup to render instead of loading a URL. |
| `fileType` | string | no | The file format to generate from the provided HTML. Default: `png`. |
| `fresh` | boolean | no | Request a newly rendered custom HTML capture instead of cached output. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customHtml": "string",
      "fileType": "string",
      "fresh": "string",
      "output": "string",
      "screenshot": "string",
      "sizes": [
        {}
      ],
      "ttl": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when ScreenshotAPI created the capture. |
| `customHtml` | string | The custom HTML markup sent to ScreenshotAPI. |
| `fileType` | string | Generated file format. |
| `fresh` | string | Whether ScreenshotAPI forced a fresh render. |
| `output` | string | Output mode returned by ScreenshotAPI. |
| `screenshot` | string | URL of the generated screenshot file. |
| `sizes` | array<object> | Optional sizes payload returned by ScreenshotAPI. |
| `ttl` | date | Expiration timestamp for the generated file. |
| `url` | string | Provider-returned source URL value for the render. |

## Native endpoint

Through the native ScreenshotAPI API, this operation is `GET /screenshot` (base URL `https://shot.screenshotapi.net/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-custom-html.md) for the provider-specific parameters and requirements.

