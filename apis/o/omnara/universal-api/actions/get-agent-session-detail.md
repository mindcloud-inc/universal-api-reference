# Omnara: Get Agent Session Detail



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-agent-session-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-agent-session-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-agent-session-detail?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "childSessions": [
        {
          "connectionStatus": "string",
          "sessionId": "string",
          "sessionType": "string",
          "workStatus": "string"
        }
      ],
      "session": {
        "connectionStatus": "string",
        "daemonVersion": "string",
        "kind": "string",
        "metadata": {},
        "parentSessionId": "string",
        "sessionId": "string",
        "sessionType": "string",
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
        "userSessionId": "string",
        "workStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childSessions` | array<object> |  |
| `childSessions[]` | object |  |
| `childSessions[].connectionStatus` | string |  |
| `childSessions[].sessionId` | string |  |
| `childSessions[].sessionType` | string |  |
| `childSessions[].workStatus` | string |  |
| `session` | object |  |
| `session.connectionStatus` | string |  |
| `session.daemonVersion` | string |  |
| `session.kind` | string |  |
| `session.metadata` | object |  |
| `session.parentSessionId` | string |  |
| `session.sessionId` | string |  |
| `session.sessionType` | string |  |
| `session.settings` | object |  |
| `session.settings.code` | object |  |
| `session.settings.code.defaultProvider` | string |  |
| `session.settings.code.mode` | string |  |
| `session.settings.code.providers` | object |  |
| `session.settings.voice` | object |  |
| `session.settings.voice.language` | string |  |
| `session.userSessionId` | string |  |
| `session.workStatus` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/user-sessions/{userSessionId}/agent-sessions/{agentSessionId}` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-session-detail.md) for the provider-specific parameters and requirements.

