# PagePixels: Capture Next Scheduled Screenshot



```
POST https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/capture-next-scheduled-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/capture-next-scheduled-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "screenshotConfigurationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/capture-next-scheduled-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "screenshotConfigurationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `screenshotConfigurationId` | string | yes | The screenshot configuration ID to capture immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embedUrl": "https://example.com",
      "jobId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embedUrl` | string | The embed URL for the screenshot configuration being captured. |
| `jobId` | string | The background job ID created for the capture. |
| `success` | boolean | Whether PagePixels accepted the immediate capture request. |

## Native endpoint

Through the native PagePixels API, this operation is `POST /screenshot_configs/:screenshot_configuration_id/capture` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-next-scheduled-screenshot.md) for the provider-specific parameters and requirements.

