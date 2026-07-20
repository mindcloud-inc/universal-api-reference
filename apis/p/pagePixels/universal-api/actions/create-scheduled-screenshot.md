# PagePixels: Create Scheduled Screenshot



```
POST https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/create-scheduled-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/create-scheduled-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "scheduledEvery": 1,
  "scheduledInterval": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/create-scheduled-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "scheduledEvery": 1,
    "scheduledInterval": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The public web page URL to schedule for screenshots. |
| `scheduledEvery` | number | yes | How often to capture the screenshot. |
| `scheduledInterval` | string | yes | The scheduler interval unit such as minutes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `multiStepActions` | string | no | JSON array of PagePixels multi-step actions, including change notification rules. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embedUrl": "https://example.com",
      "jobId": "string",
      "screenshotConfigurationId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embedUrl` | string | The embed URL for the created screenshot configuration. |
| `jobId` | string | The background job ID started for the initial capture. |
| `screenshotConfigurationId` | string | The created screenshot configuration ID. |
| `success` | boolean | Whether PagePixels accepted the scheduled screenshot creation request. |

## Native endpoint

Through the native PagePixels API, this operation is `POST /screenshot_configs` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scheduled-screenshot.md) for the provider-specific parameters and requirements.

