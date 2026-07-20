# Firecrawl: Create Browser Session

Creates a browser session in Firecrawl.

```
POST https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/create-browser-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/create-browser-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/create-browser-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ttl` | number | no | Total time-to-live in seconds for the browser session |
| `activityTtl` | number | no | Time in seconds before the session is destroyed due to inactivity |
| `streamWebView` | boolean | no | Whether to stream a live view of the browser |
| `profile` | object | no | Persistent browser profile settings |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cdpUrl": "https://example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "interactiveLiveViewUrl": "https://example.com",
      "liveViewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cdpUrl` | string |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `interactiveLiveViewUrl` | string |  |
| `liveViewUrl` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /browser` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-browser-session.md) for the provider-specific parameters and requirements.

