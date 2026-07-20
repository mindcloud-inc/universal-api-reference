# Hyperbrowser: Get Session



```
GET https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-session?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/get-session?${params}`, {
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
| `id` | string | yes | Session identifier. |

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

Through the native Hyperbrowser API, this operation is `GET /api/session/:id` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

