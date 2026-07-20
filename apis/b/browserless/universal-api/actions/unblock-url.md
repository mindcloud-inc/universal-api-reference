# Browserless: Unblock Url

Retrieves page content from blocked sites in Browserless.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/unblock-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/unblock-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/unblock-url?${params}`, {
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
| `url` | string | yes | The URL of the site to unblock. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | boolean | no | Whether to return HTML content in the unblock response. |
| `cookies` | boolean | no | Whether to return cookies in the unblock response. |
| `screenshot` | boolean | no | Whether to return a full-page screenshot in the unblock response. |
| `browserWSEndpoint` | boolean | no | Whether to keep the browser alive and return a browserWSEndpoint for reconnects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserWSEndpoint": "string",
      "content": "string",
      "screenshot": "string",
      "ttl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserWSEndpoint` | string | Reconnect endpoint returned when Browserless keeps the browser session alive. |
| `content` | string | HTML content returned by Browserless when content capture is enabled. |
| `screenshot` | string | Base64 screenshot returned when screenshot capture is enabled. |
| `ttl` | number | Browser session time-to-live reported by Browserless. |

## Native endpoint

Through the native Browserless API, this operation is `POST /unblock` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unblock-url.md) for the provider-specific parameters and requirements.

