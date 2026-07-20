# OnceOnly: Create or Update Tool

Creates or updates a tool in OnceOnly.

```
POST https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-or-update-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceOnly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-or-update-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "scopeId": "global",
  "url": "https://example.com",
  "auth": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-or-update-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "scopeId": "global",
    "url": "https://example.com",
    "auth": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Tool name. |
| `scopeId` | string | yes | Tool scope, such as global or agent:agent_id. Default: `global`. |
| `url` | string | yes | Tool endpoint URL. |
| `auth` | object | yes | Auth object. Set type to hmac_sha256 and include secret. |
| `timeoutMs` | number | no | Request timeout in milliseconds. Default: `15000`. |
| `maxRetries` | number | no | Retry count. Default: `2`. |
| `enabled` | boolean | no | Whether the tool is enabled. Default: `true`. |
| `description` | string | no | Optional tool description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceOnly API returns.

## Native endpoint

Through the native OnceOnly API, this operation is `POST /v1/tools` (base URL `https://api.onceonly.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-tool.md) for the provider-specific parameters and requirements.

