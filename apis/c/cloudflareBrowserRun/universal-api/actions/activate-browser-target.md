# Cloudflare Browser Run: Activate Browser Target

Activates a browser target in Cloudflare Browser Run.

```
PUT https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/activate-browser-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/activate-browser-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "targetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/activate-browser-target', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "targetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Browser session ID. |
| `targetId` | string | yes | Chrome DevTools target ID to activate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/activate/:targetId` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-browser-target.md) for the provider-specific parameters and requirements.

