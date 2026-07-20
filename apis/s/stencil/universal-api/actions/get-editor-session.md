# Stencil: Get Editor Session



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-editor-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-editor-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-editor-session?${params}`, {
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
| `sessionId` | string | yes | Editor session ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "permissions": {},
      "sessionId": "string",
      "sessionUrl": "https://example.com",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiredAt` | date |  |
| `permissions` | object |  |
| `sessionId` | string |  |
| `sessionUrl` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Stencil API, this operation is `GET /v1/editor/sessions/:session_id` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-editor-session.md) for the provider-specific parameters and requirements.

