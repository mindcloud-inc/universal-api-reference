# ScreenshotAPI: Record Multiple Scrolling Screenshots

Creates multiple scrolling screenshot recordings in ScreenshotAPI.

```
POST https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/record-multiple-scrolling-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/record-multiple-scrolling-screenshots" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "sizes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/record-multiple-scrolling-screenshots', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "sizes": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The fully qualified URL to record at multiple target sizes. |
| `fileType` | string | no | The scrolling capture file format. Default: `mp4`. |
| `sizes` | string | yes | JSON array string describing the output sizes to generate. |
| `fresh` | boolean | no | Request a newly rendered scrolling capture instead of cached output. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileType": "string",
      "fresh": "string",
      "multipleScrolling": "string",
      "output": "string",
      "screenshot": {},
      "scrollingScreenshot": "string",
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
| `multipleScrolling` | string | Whether multiple scrolling mode was enabled. |
| `output` | string | Output mode returned by ScreenshotAPI. |
| `screenshot` | object | Object of generated file URLs keyed by size identifier. |
| `scrollingScreenshot` | string | Whether scrolling mode was enabled. |
| `sizes` | array<object> | Requested output sizes returned by ScreenshotAPI. |
| `ttl` | date | Expiration timestamp for the generated files. |
| `url` | string | Captured page URL returned by ScreenshotAPI. |

## Native endpoint

Through the native ScreenshotAPI API, this operation is `GET /screenshot` (base URL `https://shot.screenshotapi.net/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-multiple-scrolling-screenshots.md) for the provider-specific parameters and requirements.

