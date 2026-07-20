# Cloudflare Browser Run: Connect DevTools Page

Retrieves DevTools page connection details from Cloudflare Browser Run.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/connect-devtools-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/connect-devtools-page?connectionId=$CONNECTION_ID&sessionId=string&targetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "targetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/connect-devtools-page?${params}`, {
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
| `targetId` | string | yes | Chrome DevTools target or page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webSocketDebuggerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webSocketDebuggerUrl` | string |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/page/:targetId` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-devtools-page.md) for the provider-specific parameters and requirements.

