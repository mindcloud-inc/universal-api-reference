# Cloudflare Browser Run: Get Screenshot

Captures a webpage screenshot in Cloudflare Browser Run.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-screenshot?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-screenshot?${params}`, {
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
| `html` | string | no | HTML content to render. Either HTML or URL must be set. |
| `url` | string | no | URL to navigate to. Either URL or HTML must be set. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `screenshotOptions` | object | no | Puppeteer screenshot options such as fullPage, clip, encoding, and type. |
| `cacheTTL` | number | no | Cache TTL in seconds. Set 0 to disable cache. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `POST /accounts/:accountId/browser-rendering/screenshot` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot.md) for the provider-specific parameters and requirements.

