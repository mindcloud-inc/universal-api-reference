# Agent.ai: Capture Web Page Screenshot

Captures a web page screenshot in Agent.ai by URL.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/capture-web-page-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/capture-web-page-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/capture-web-page-screenshot?${params}`, {
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
| `url` | string | yes | URL of the web page to capture. |
| `ttlForScreenshot` | number | no | Cache expiration time for the screenshot in seconds. Default: `86400`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `response` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/grab_web_screenshot` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-web-page-screenshot.md) for the provider-specific parameters and requirements.

