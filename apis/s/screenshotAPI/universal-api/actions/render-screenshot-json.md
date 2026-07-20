# ScreenshotAPI: Render Screenshot JSON

Creates screenshot metadata in ScreenshotAPI with selectable file output.

```
POST https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/render-screenshot-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/render-screenshot-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/render-screenshot-json', {
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
| `url` | string | yes | The fully qualified URL to capture. |
| `fileType` | string | no | The screenshot file format to generate. Default: `png`. |
| `fresh` | boolean | no | When true, request a newly rendered screenshot instead of cached output. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
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
| `fileType` | string | Generated file format. |
| `fresh` | string | Whether ScreenshotAPI forced a fresh render. |
| `output` | string | Output mode returned by ScreenshotAPI. |
| `screenshot` | string | URL of the generated screenshot file. |
| `sizes` | array<object> | Optional sizes payload returned by ScreenshotAPI. |
| `ttl` | date | Expiration timestamp for the generated file. |
| `url` | string | Captured page URL returned by ScreenshotAPI. |

## Native endpoint

Through the native ScreenshotAPI API, this operation is `GET /screenshot` (base URL `https://shot.screenshotapi.net/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-screenshot-json.md) for the provider-specific parameters and requirements.

