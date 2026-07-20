# Omnara: Update User Session



```
PUT https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-user-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-user-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-user-session', {
  method: 'PUT',
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
      "createdAt": "string",
      "kind": "string",
      "metadata": {},
      "name": "Ava Chen",
      "sessionId": "string",
      "settings": {
        "code": {
          "defaultProvider": "string",
          "mode": "string",
          "providers": {
            "claudeCode": {},
            "codex": {}
          }
        },
        "voice": {
          "language": "string"
        }
      },
      "status": "string",
      "userId": "string",
      "worktreeId": "string",
      "worktreeName": "Ava Chen",
      "worktreeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `kind` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `sessionId` | string |  |
| `settings` | object |  |
| `settings.code` | object |  |
| `settings.code.defaultProvider` | string |  |
| `settings.code.mode` | string |  |
| `settings.code.providers` | object |  |
| `settings.code.providers.claudeCode` | object |  |
| `settings.code.providers.codex` | object |  |
| `settings.voice` | object |  |
| `settings.voice.language` | string |  |
| `status` | string |  |
| `userId` | string |  |
| `worktreeId` | string |  |
| `worktreeName` | string |  |
| `worktreeType` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `PATCH /api/v1/user-sessions/{userSessionId}` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-session.md) for the provider-specific parameters and requirements.

