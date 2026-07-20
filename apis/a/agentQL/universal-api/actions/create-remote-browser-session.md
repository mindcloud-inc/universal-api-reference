# AgentQL: Create Remote Browser Session

Creates a remote browser session with CDP access in AgentQL.

```
POST https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/create-remote-browser-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AgentQL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/create-remote-browser-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/create-remote-browser-session', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browserUaPreset` | string | no |  |
| `browserProfile` | string | no |  |
| `shutdownMode` | string | no |  |
| `inactivityTimeoutSeconds` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subUserId` | string | no |  |
| `proxy` | object | no |  |
| `proxy.type` | string | no |  |
| `proxy.countryCode` | string | no |  |
| `proxy.url` | string | no |  |
| `proxy.username` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AgentQL API returns.

## Native endpoint

Through the native AgentQL API, this operation is `POST /v1/tetra/sessions` (base URL `https://api.agentql.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-remote-browser-session.md) for the provider-specific parameters and requirements.

