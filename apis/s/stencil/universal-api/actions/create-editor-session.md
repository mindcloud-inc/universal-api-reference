# Stencil: Create Editor Session



```
POST https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-editor-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-editor-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "expires": 1,
  "name": "Ava Chen",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-editor-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "expires": 1,
    "name": "Ava Chen",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expires` | number | yes | Time until expiration in seconds. |
| `name` | string | yes | Name of the editor session. |
| `permissions` | object | no | Optional permissions object for the editor session. |
| `templateId` | string | yes | Template ID to give edit access to. |

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

Through the native Stencil API, this operation is `POST /v1/editor/sessions` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-editor-session.md) for the provider-specific parameters and requirements.

