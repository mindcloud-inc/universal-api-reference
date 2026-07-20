# Pachca (Admin): Request Chat Export

Requests a chat export from the Pachca Admin API.

```
POST https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/request-chat-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/request-chat-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "startAt": "2026-05-07T12:00:00.000Z",
  "endAt": "2026-05-07T12:00:00.000Z",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/request-chat-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "startAt": "2026-05-07T12:00:00.000Z",
    "endAt": "2026-05-07T12:00:00.000Z",
    "webhookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startAt` | date | yes |  |
| `endAt` | date | yes |  |
| `webhookUrl` | string | yes |  |
| `chatIds[]` | array<number> | no |  |
| `skipChatsFile` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `POST /chats/exports` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-chat-export.md) for the provider-specific parameters and requirements.

