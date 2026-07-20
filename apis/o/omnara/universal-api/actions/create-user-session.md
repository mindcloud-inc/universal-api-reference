# Omnara: Create User Session



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/create-user-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/create-user-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/create-user-session', {
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
      "agentSessions": [
        {
          "connectionStatus": "string",
          "daemonVersion": "string",
          "kind": "string",
          "metadata": {},
          "parentSessionId": "string",
          "sessionId": "string",
          "sessionType": "string",
          "settings": {},
          "userSessionId": "string",
          "workStatus": "string"
        }
      ],
      "session": {
        "createdAt": "string",
        "kind": "string",
        "metadata": {},
        "name": "Ava Chen",
        "sessionId": "string",
        "settings": {
          "code": {
            "defaultProvider": "string",
            "mode": "string",
            "providers": {}
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
      },
      "workspace": {
        "gitHost": "string",
        "gitPath": "string",
        "id": "string",
        "userId": "string",
        "workspaceConfig": {},
        "workspaceMetadata": {}
      },
      "worktree": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentSessions` | array<object> |  |
| `agentSessions[]` | object |  |
| `agentSessions[].connectionStatus` | string |  |
| `agentSessions[].daemonVersion` | string |  |
| `agentSessions[].kind` | string |  |
| `agentSessions[].metadata` | object |  |
| `agentSessions[].parentSessionId` | string |  |
| `agentSessions[].sessionId` | string |  |
| `agentSessions[].sessionType` | string |  |
| `agentSessions[].settings` | object |  |
| `agentSessions[].userSessionId` | string |  |
| `agentSessions[].workStatus` | string |  |
| `session` | object |  |
| `session.createdAt` | string |  |
| `session.kind` | string |  |
| `session.metadata` | object |  |
| `session.name` | string |  |
| `session.sessionId` | string |  |
| `session.settings` | object |  |
| `session.settings.code` | object |  |
| `session.settings.code.defaultProvider` | string |  |
| `session.settings.code.mode` | string |  |
| `session.settings.code.providers` | object |  |
| `session.settings.voice` | object |  |
| `session.settings.voice.language` | string |  |
| `session.status` | string |  |
| `session.userId` | string |  |
| `session.worktreeId` | string |  |
| `session.worktreeName` | string |  |
| `session.worktreeType` | string |  |
| `workspace` | object |  |
| `workspace.gitHost` | string |  |
| `workspace.gitPath` | string |  |
| `workspace.id` | string |  |
| `workspace.userId` | string |  |
| `workspace.workspaceConfig` | object |  |
| `workspace.workspaceMetadata` | object |  |
| `worktree` | object |  |
| `worktree.id` | string |  |
| `worktree.name` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/user-sessions` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-session.md) for the provider-specific parameters and requirements.

