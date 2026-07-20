# Cloudflare Browser Run: Get Browser Version

Retrieves browser version details from Cloudflare Browser Run.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-browser-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-browser-version?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-browser-version?${params}`, {
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
| `sessionId` | string | yes | Browser session ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Browser": "string",
      "Protocol-Version": "string",
      "User-Agent": "string",
      "V8-Version": "string",
      "WebKit-Version": "string",
      "webSocketDebuggerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Browser` | string |  |
| `Protocol-Version` | string |  |
| `User-Agent` | string |  |
| `V8-Version` | string |  |
| `WebKit-Version` | string |  |
| `webSocketDebuggerUrl` | string |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/version` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browser-version.md) for the provider-specific parameters and requirements.

