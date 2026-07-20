# PagePixels: Get Job Status



```
GET https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | The PagePixels job ID returned by create or capture endpoints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai": {},
      "directLink": "https://example.com",
      "directThumbnailLink": "https://example.com",
      "embedUrl": "https://example.com",
      "id": "string",
      "isBrowserExtensionScreenshot": true,
      "jobId": "string",
      "screenshotConfigurationId": "string",
      "takenAt": "string",
      "takenAtTimestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai` | object | The nested AI analysis metadata returned with the screenshot. |
| `directLink` | string | The direct CDN URL for the generated screenshot image. |
| `directThumbnailLink` | string | The direct CDN URL for the generated screenshot thumbnail. |
| `embedUrl` | string | The embed URL for the screenshot or screenshot configuration. |
| `id` | string | The screenshot record ID returned by PagePixels. |
| `isBrowserExtensionScreenshot` | boolean | Whether the screenshot came from the browser extension flow. |
| `jobId` | string | The background job ID associated with the screenshot. |
| `screenshotConfigurationId` | string | The screenshot configuration ID associated with the captured screenshot. |
| `takenAt` | string | The ISO-like timestamp for when the screenshot was captured. |
| `takenAtTimestamp` | string | The capture timestamp value returned by PagePixels. |

## Native endpoint

Through the native PagePixels API, this operation is `GET /jobs/:job_id` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

