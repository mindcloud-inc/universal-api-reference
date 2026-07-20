# ScreenshotAPI: Record Scrolling Screenshot

Creates a scrolling screenshot recording in ScreenshotAPI.

```
POST https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/record-scrolling-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/record-scrolling-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/record-scrolling-screenshot', {
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
| `url` | string | yes | The fully qualified URL to record as a scrolling screenshot. |
| `fileType` | string | no | The scrolling capture file format. Default: `mp4`. |
| `scrollSpeed` | string | no | Control how quickly the page scrolls during capture. Default: `normal`. |
| `duration` | number | no | Capture duration in seconds for the scrolling recording. |
| `scrollBack` | boolean | no | Scroll back to the top after reaching the bottom of the page. Default: `false`. |
| `startImmediately` | boolean | no | Begin recording immediately without waiting for page load. Default: `false`. |
| `fresh` | boolean | no | Request a newly rendered scrolling capture instead of cached output. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "fileType": "string",
      "fresh": "string",
      "output": "string",
      "screenshot": "string",
      "scrollBack": "string",
      "scrollingScreenshot": "string",
      "scrollSpeed": "string",
      "sizes": [
        {}
      ],
      "startImmediately": "string",
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
| `duration` | string | Requested capture duration in seconds. |
| `fileType` | string | Generated file format. |
| `fresh` | string | Whether ScreenshotAPI forced a fresh render. |
| `output` | string | Output mode returned by ScreenshotAPI. |
| `screenshot` | string | URL of the generated scrolling video file. |
| `scrollBack` | string | Whether the capture scrolled back to the top. |
| `scrollingScreenshot` | string | Whether scrolling mode was enabled. |
| `scrollSpeed` | string | Scroll speed used for the capture. |
| `sizes` | array<object> | Optional sizes payload returned by ScreenshotAPI. |
| `startImmediately` | string | Whether recording started immediately. |
| `ttl` | date | Expiration timestamp for the generated file. |
| `url` | string | Captured page URL returned by ScreenshotAPI. |

## Native endpoint

Through the native ScreenshotAPI API, this operation is `GET /screenshot` (base URL `https://shot.screenshotapi.net/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-scrolling-screenshot.md) for the provider-specific parameters and requirements.

