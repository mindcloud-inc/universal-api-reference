# Browser Use: Get Browser Session

Retrieves a browser session from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-browser-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-browser-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-browser-session?${params}`, {
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
      "cdpUrl": "https://example.com",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "liveUrl": "https://example.com",
      "recordingUrl": "https://example.com",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cdpUrl` | string |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `liveUrl` | string |  |
| `recordingUrl` | string |  |
| `startedAt` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Browser Use API, this operation is `GET /browsers/:session_id` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browser-session.md) for the provider-specific parameters and requirements.

