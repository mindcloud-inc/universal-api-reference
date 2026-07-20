# Cloudflare Browser Run: Open Browser Tab

Opens a new browser tab in Cloudflare Browser Run.

```
POST https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/open-browser-tab
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/open-browser-tab" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/open-browser-tab', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Browser session ID. |
| `url` | string | no | Optional URL to open in the new browser tab. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "devtoolsFrontendUrl": "https://example.com",
      "id": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "webSocketDebuggerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `devtoolsFrontendUrl` | string |  |
| `id` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `webSocketDebuggerUrl` | string |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `PUT /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/new` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-browser-tab.md) for the provider-specific parameters and requirements.

