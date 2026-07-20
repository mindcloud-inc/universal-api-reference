# Hyperbrowser: Create Session



```
POST https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/create-session', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "computerActionEndpoint": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditBreakdown": {},
      "id": "string",
      "launchState": {},
      "liveDomain": "string",
      "liveUrl": "https://example.com",
      "sessionUrl": "https://example.com",
      "status": "string",
      "teamId": "string",
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webdriverEndpoint": "string",
      "wsEndpoint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `computerActionEndpoint` | string |  |
| `createdAt` | date |  |
| `creditBreakdown` | object |  |
| `id` | string |  |
| `launchState` | object |  |
| `liveDomain` | string |  |
| `liveUrl` | string |  |
| `sessionUrl` | string |  |
| `status` | string |  |
| `teamId` | string |  |
| `token` | string |  |
| `updatedAt` | date |  |
| `webdriverEndpoint` | string |  |
| `wsEndpoint` | string |  |

## Native endpoint

Through the native Hyperbrowser API, this operation is `POST /api/session` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

