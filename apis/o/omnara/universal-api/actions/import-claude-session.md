# Omnara: Import Claude Session



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/import-claude-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/import-claude-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/import-claude-session', {
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
      "agentSessionId": "string",
      "error": "string",
      "messageCount": 1,
      "success": true,
      "userSessionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentSessionId` | string |  |
| `error` | string |  |
| `messageCount` | number |  |
| `success` | boolean |  |
| `userSessionId` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/user-sessions/import-claude-session` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-claude-session.md) for the provider-specific parameters and requirements.

