# Anchor: Get Browser Session

Retrieves a browser session from Anchor.

```
GET https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-browser-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-browser-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-browser-session?${params}`, {
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
| `sessionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "credits_used": 1,
      "duration": 1,
      "playground": true,
      "proxy_bytes": 1,
      "session_id": "string",
      "status": "string",
      "team_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `credits_used` | number |  |
| `duration` | number |  |
| `playground` | boolean |  |
| `proxy_bytes` | number |  |
| `session_id` | string |  |
| `status` | string |  |
| `team_id` | string |  |

## Native endpoint

Through the native Anchor API, this operation is `GET /v1/sessions/:sessionId` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browser-session.md) for the provider-specific parameters and requirements.

